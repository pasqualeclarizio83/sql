# SQL

Breve guida su SQL

## Descrizione

Crea una tabella in SQL di una Persona

```bash
# Esempio
CREATE TABLE Persona (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(50) NOT NULL,
    cognome VARCHAR(50) NOT NULL,
    data_di_nascita DATE,
    indirizzo VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    telefono VARCHAR(20)
);

```


## Descrizione
Crea una tabella in SQL di una Persona
e del suo biglietto

```bash
# Esempio
-- Tabella Persona
CREATE TABLE Persona (
    id_persona INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(50) NOT NULL,
    cognome VARCHAR(50) NOT NULL,
    data_di_nascita DATE,
    indirizzo VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    telefono VARCHAR(20)
);

-- Tabella Biglietto
CREATE TABLE Biglietto (
    id_biglietto INT PRIMARY KEY AUTO_INCREMENT,
    id_persona INT,
    FOREIGN KEY (id_persona) REFERENCES Persona(id_persona),
    tipo VARCHAR(50) NOT NULL,
    data_acquisto DATE,
    prezzo DECIMAL(10, 2) NOT NULL
);

```


## Descrizione
Crea una tabella che rappresenta la Mamma
Ma la Mamma può avere un solo Uomo

```bash
# Esempio
-- Tabella Mamma
CREATE TABLE Mamma (
    id_mamma INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(50) NOT NULL,
    cognome VARCHAR(50) NOT NULL,
    data_di_nascita DATE,
    indirizzo VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    telefono VARCHAR(20),
    id_uomo INT UNIQUE,
    FOREIGN KEY (id_uomo) REFERENCES Uomo(id_uomo)
);

-- Tabella Uomo
CREATE TABLE Uomo (
    id_uomo INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(50) NOT NULL,
    cognome VARCHAR(50) NOT NULL,
    data_di_nascita DATE,
    indirizzo VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    telefono VARCHAR(20)
);

```
