# Teste Prático Java

Construir uma solução para busca de CEP.


## Fontes
 - Utilizar a API aberta [Via Cep](https://viacep.com.br/) para as buscas de CEP
 - Utilizar a API aberta [Brasil API](https://brasilapi.com.br/) para as buscas dos dados do estado


## Especificações
 - desenvolver rotina que periodicamente busque na API **Via Cep** CEP’s aleatórios. (A cada minuto, buscar 5 CEP’s aleatórios para compor a base);
 - alterar as execuções de consultas na API **Via Cep** nos tipos de retorno (XML, PIPED e JSON); 
 - os retornos devem ser persistidos em banco de dados;
 - caso o CEP montado aleatoriamente já esteja persistido no banco de dados, deverá ser gerado uma nova combinação;
 - complementar as informações dos estados utilizando a API **Brasil API**; 


## endpoints expostos
 - busca do CEP (apenas os dígitos): deverá verificar se o CEP já está cadastrado no banco e, caso não esteja ou o **tempo cadastrado seja superior a 5 minutos**, deverá buscar na API de CEP;
 - busca de todos os CEP’s: agrupar e retornar os CEP's por estado (UF);
 - busca por estado (UF): agrupar e retornar os CEP's por cidade;
 - busca por cidade: retornar todos os CEP's da cidade;


## regras
 - padronizar response em json;
 - readme com explicação da estrutura do projeto, configuração para execução, etc;
 - a entrega deverá ser feita via repositório compartilhado (github, gitlab, etc);
 - documentar o projeto;


## diferenciais (não necessariamente precisa expor isso pro candidato, podem servir de parametros de análise)
 - parametrização de CI/CD;
 - entrega da aplicação containerizada e rodando em cloud;
 - desenvolvimento de testes (TDD);


## específicos para o ultron (discutir se levantamos esses pontos pro candidato ou não)
 - operações de banco de dados devem ser realizadas sem auxílio de ORM (utilizar JDBC);
 - as queries performadas devem ficar num arquivo de configuração;
 - utilizar preferencialmente SQL Server;
 - trabalhar concurrentemente;


# Essa parte não vai para o candidato, direcionamento interno explicando como o teste foi pensado

## itens avaliados
 - padronização e organização;
 - escrita de código;
 - documentação;
 - controle de fluxo;
 - criatividade na resolução de problemas;
 - patterns e anti-patterns;
 - funcionamento e funcionalidades;
 - nível de conhecimento arquiteturial;

## Motivos
 - identificação do perfil de desenvolvedor;
 - vícios antigos;
 - nível de lógica e resolução de problemas;
 - controle de dados;
 - fluxo: interpretação -> análise -> desenvolvimento (o teste é meio vago justamente por isso);
 - conhecimentos gerais de desenvolvimento;
 - identificação do nível de conhecimentos específicos da linguagem e seus recursos;
