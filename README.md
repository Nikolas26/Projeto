create database pokedex;

use pokedex;

create table pokemon(
	nome varcharacter(50) not null,
    id int (3) not null,
    tipo varcharacter(50),
    tipo_sec varcharacter(50),
    altura float(5,2),
    peso float(5,2),
	vida int (3),
    atq int (3),
    def int (3),
    sp_atq int (3),
    sp_def int (3),
    veloc int (3),
	regiao varcharacter(50),
    descricao varcharacter(150),
	foreign key (tipo) references tipos(nome_tipo),
    foreign key (regiao) references regioes(nome_regiao),
    primary key (id) 
);

create table tipos(
    nome_tipo varcharacter(50) not null primary key
);

create table regioes(
	nome_regiao varcharacter(50) primary key
);

select * from regioes;

#insert de regiao
INSERT INTO `pokedex`.`regioes` (`nome_regiao`) VALUES ('kanto');
INSERT INTO `pokedex`.`regioes` (`nome_regiao`) VALUES ('johto');
INSERT INTO `pokedex`.`regioes` (`nome_regiao`) VALUES ('hoenn');
INSERT INTO `pokedex`.`regioes` (`nome_regiao`) VALUES ('sinnoh');
INSERT INTO `pokedex`.`regioes` (`nome_regiao`) VALUES ('unova');
INSERT INTO `pokedex`.`regioes` (`nome_regiao`) VALUES ('kalos');
INSERT INTO `pokedex`.`regioes` (`nome_regiao`) VALUES ('alola');
INSERT INTO `pokedex`.`regioes` (`nome_regiao`) VALUES ('galar');
INSERT INTO `pokedex`.`regioes` (`nome_regiao`) VALUES ('hisui');
INSERT INTO `pokedex`.`regioes` (`nome_regiao`) VALUES ('paldea');
INSERT INTO `pokedex`.`regioes` (`nome_regiao`) VALUES ('mogi das cruzes');

#inserts de tipo
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('fogo');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('água');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('terra');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('pedra');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('planta');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('veneno');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('voador');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('gelo');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('metal');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('lutador');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('dragão');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('fada');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('psíquico');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('fantasma');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('sombrio');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('elétrico');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('normal');
INSERT INTO `pokedex`.`tipos` (`nome_tipo`) VALUES ('inseto');


INSERT INTO `pokedex`.`pokemon` (`nome`,`id`,`tipo`,`tipo_sec`,`altura`,`peso`,`vida`,`atq`,`def`,`sp_atq`,`sp_def`,`veloc`,`regiao`,`descricao`) VALUES ('Bulbasaur','001','planta','veneno','0.40','4','45','49','49','65','65','45','kanto','Bulbasaur é um Pokémon bonito nascido com uma grande semente solidamente fixado à sua volta, a semente cresce em tamanho como o Pokémon tem.');
