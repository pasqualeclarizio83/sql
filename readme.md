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