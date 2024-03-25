# SqlGuilherme_test

use guilherme_test;

alter table tbcliente add primary key (cpf);

alter table tbcliente add column (data_nascimento DATE);

describe tbcliente;

INSERT INTO `guilherme_test`.`tbcliente`
(`cpf`,
`nome`,
`endereco1`,
`endereço2`,
`bairro`,
`cidade`,
`estado`,
`cep`,
`idade`,
`sexo`,
`limite_credito`,
`volume_compra`,
`primeira_compra`,
`data_nascimento`)
VALUES
('11122233344', 'Lucas Oliveira', 'Rua das Palmeiras', 'Apt. 301', 'Centro', 'Belo Horizonte', 'MG', '31234567', 25, 'm', 2000.00, 50.25, b'1', '1999-03-10'),
('22233344455', 'Mariana Santos', 'Av. das Américas', 'Bloco C', 'Barra da Tijuca', 'Rio de Janeiro', 'RJ', '22789012', 28, 'f', 3500.00, 80.30, b'0', '1994-07-22'),
('33344455566', 'Rafaela Costa', 'Rua da Praia', 'Casa 15', 'Praia Grande', 'Santos', 'SP', '11122334', 32, 'f', 4000.00, 90.75, b'1', '1989-12-05'),
('44455566677', 'Gustavo Silva', 'Rua das Flores', 'Apt. 102', 'Centro', 'São Paulo', 'SP', '01234567', 35, 'm', 5000.00, 120.60, b'1', '1987-04-18'),
('55566677788', 'Fernanda Vieira', 'Av. das Árvores', 'Casa 20', 'Bosque dos Ipês', 'Campo Grande', 'MS', '79012345', 40, 'f', 4500.00, 100.00, b'0', '1982-11-30');

select * from tbcliente;

select cpf, nome from tbcliente limit 5;

SELECT * FROM tbproduto WHERE PRECO_LISTA BETWEEN 16.007 AND 16.009;

SELECT * FROM tbcliente WHERE IDADE >= 18 AND IDADE <= 22 AND SEXO = 'M';

SELECT * FROM tbcliente WHERE cidade = 'Rio de Janeiro' OR BAIRRO = 'Jardins';

SELECT * FROM tbcliente WHERE (IDADE >= 18 AND IDADE <= 22 AND SEXO = 'M')
 OR (cidade = 'Rio de Janeiro' OR BAIRRO = 'Jardins');
