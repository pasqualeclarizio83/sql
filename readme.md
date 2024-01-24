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