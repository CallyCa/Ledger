# ADR: Fixar Versão .NET e PostgreSQL
Essa decisão foi influenciada pela necessidade de manter a reprodutibilidade do projeto ao longo do tempo e evitar divergências 
em diferentes ambientes de desenvolvimento, integração contínua e produção. Ao definir uma versão fixa do .NET e PostgreSQL, podemos
garantir que o projeto não irá sofrera dos problemas previamente citados.

## Decisão 
O projeto utilizará .NET 10 LTS, com target framework net10.0. A versão do SDK será definida em um arquivo global.json, permitindo atualizações compatíveis conforme a política de rollForward adotada.



## Justificativa
De acordo com a política de suporte da Microsoft, a versão 10 do .NET é a versão LTS (Long-Term Support) mais recente, com garantia
de suporte até 14 de novembro de 2028. Ao escolher essa versão podemos garantir estabilidade da plataforma pelo maior tempo possível
assim como garantia de maior número de  patches de segurança e evita a necessidade de atualizações anuais do framework. Quanto ao
PostgreSQL, a versão "major" mais recente lançada é a 18, de acordo com a politica de versões do PostgreSQL Global Development Group,
cada versão recebe suporte por 5 anos após seu lançamento, recebendo versões "minor" com correções de bugs e vulnerabilidades a cada
3 meses. A versão 18 foi lançada no dia 25 de setembro de 2025, e tem suporte garantido até 14 de novembro de 2030. Escolher essa
versão garante estabilidade e acesso as funcionalidades mais lançadas mais recentemente, evitando a necessidade de atualizações e risco
de breaking changes tão cedo.


## Status
[Proposta]


## Consequências
A definição das versões estabelece uma base comum para desenvolvimento, testes e execução, reduzindo divergências entre os ambientes. A compatibilidade com os demais ambientes de desenvolvimento continuarão sendo acompanhadas conforme as políticas oficiais de suporte.

### Positivas
- Disponibilizará as ferramentas mais recentes na plataforma .NET e o sistema de gerenciamento de banco de dados PostgreSQL
- Garantirá a correção de bugs e recebimento de patches de segurança pelo maior período possível
- Maior desempenho do código devida as otimizações implementadas a cada versão lançada

### Negativas
- Bibliotecas desatualizadas podem não ser compatíveis com uma versão mais recente da plataforma .NET ou PostgreSQL
- Tempo de adaptação do desenvolvedor às novas ferramentas disponibilizadas nessa versão escolhida

## Referências (aqui é para termos algo mais rastreável)
- Política de versionamento PostgreSQL: https://www.postgresql.org/support/versioning/
- Política de versionamento .NET: https://dotnet.microsoft.com/en-us/platform/support/policy
## Data da consulta
21/07/2026