# MyJure Agente — versões

Este repositório guarda **apenas os instaladores** do MyJure Agente, o
aplicativo de mesa que lê andamentos direto no sistema do tribunal, no
computador do escritório, com uma pessoa disponível para a verificação que o
tribunal às vezes pede.

O código-fonte não mora aqui.

## Por que ele é público

O agente se atualiza sozinho, e para isso o pacote precisa de um endereço que
não peça autenticação. É a mesma distribuição de qualquer aplicativo de
desktop.

**O instalador não carrega segredo nenhum.** O token do escritório é digitado
na primeira execução e guardado no Gerenciador de Credenciais do Windows, na
máquina — nunca no pacote, nunca em arquivo.

## Como as atualizações são verificadas

Cada pacote vai acompanhado de um `.sig`. O agente confere essa assinatura com
a chave pública embutida nele antes de instalar qualquer coisa: pacote sem
assinatura válida é recusado, venha de onde vier.

## Instalação

Baixe o `.exe` da versão mais recente em
[Releases](../../releases/latest) e execute. Depois desta vez, o agente se
encarrega: ele procura versão nova de 6 em 6 horas e instala fora das
rodadas de leitura.
