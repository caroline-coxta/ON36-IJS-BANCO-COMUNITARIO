# ON36-IJS-BANCO-COMUNITARIO
Projeto de banco comunitário - Reprograma

Resumo
O Banco Cultivo tem como objetivo diminuir a distância entre a produção e a mesa das pessoas, promover o desenvolvimento sustentável e a inclusão financeira de pequenos agricultores e comunidades rurais. Este banco comunitário se diferencia pelo seu foco em fortalecer a economia local, oferecendo produtos e serviços financeiros adaptados às necessidades específicas dos agricultores familiares e pequenos produtores. Além disso, busca-se promover a sustentabilidade ambiental, a justiça social e a viabilidade econômica ao valorizar os conhecimentos tradicionais e inovadores dos pequenos agricultores, ao mesmo tempo em que preserva e restaura os ecossistemas.

Classes

1. Usuario
  `id` INT UNSIGNED NOT NULL AUTO_INCREMENT,
  `nome_completo` VARCHAR(255) NOT NULL,
  `data_de_nascimento` DATE NOT NULL,
  `cpf` VARCHAR(255) NOT NULL,
  `endereco` TEXT NOT NULL,
  `email` VARCHAR(255) NOT NULL,
  `telefone` VARCHAR(255) NULL,
  `conta_id` INT UNSIGNED NOT NULL,
  `conta_numero_da_conta` VARCHAR(255) NOT NULL,

2. Conta
  `id` INT UNSIGNED NOT NULL AUTO_INCREMENT,
  `numero_da_conta` VARCHAR(255) NOT NULL,
  `numero_da_agencia` VARCHAR(255) NOT NULL,
  `tipo_de_conta` TINYINT(1) NOT NULL,
  `saldo` FLOAT NOT NULL,

3. Movimentações
  `id` INT UNSIGNED NOT NULL AUTO_INCREMENT,
  `credito` FLOAT NULL,
  `debito` FLOAT NULL,
  `origem` VARCHAR(255) NULL,
  `conta_id` INT UNSIGNED NOT NULL,
  `conta_numero_da_conta` VARCHAR(255) NOT NULL,

4. Linhas de crédito
CREATE TABLE IF NOT EXISTS `reprograma`.`linhas_de_credito` (
  `id` INT UNSIGNED NOT NULL AUTO_INCREMENT,
  `tipo_de_credito` VARCHAR(45) NULL,
  `conta_id` INT UNSIGNED NOT NULL,
  `valor_emprestad` INT NOT NULL,
  `numero_parcelas` INT NOT NULL,
  `juros` FLOAT NOT NULL,

   
