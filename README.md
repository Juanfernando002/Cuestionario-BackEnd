# Cuestionario-BackEnd
create database db_cuestionario;
CREATE TABLE tblcuestionario(
PKId int(10) auto increment PRIMARY KEY,
Nombre_del_cuestionario VARCHAR(100) NOT NULL,
descripcion_del_cuestionario VARCHAR(1000) NULL
);

CREATE TABLE tblpreguntas(
PKId int(10) auto increment PRIMARY KEY,
Pregunta VARCHAR(1000) NOT NULL,
FKId_tblcuestionario NOT NULL,
);

CREATE TABLE tblrespuestapreguntas(
PKId double(20) auto increment PRIMARY KEY,
Respuestas VARCHAR(1000) NOT NULL,
FKId_pregunta NOT NULL,
FKId_tblcuestionario NOT NULL,
FKId_Nombre NOT NULL,
FKId NOT NULL,
FKId_fecha NOT NULL
);

CREATE TABLE tblencuestados(
PKId (10) auto increment PRIMARY KEY,
Nombre_del_encuestado VARCHAR(1000) NOT NULL,
CC_encuestado NOT NULL,
Fecha_de_encuesta NOT NULL
);
