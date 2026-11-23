# Agendador do CommentFlow

Este repositório existe por um motivo só: bater de 5 em 5 minutos no
agendador do painel, em https://commentflow-delta.vercel.app.

A Vercel, no plano gratuito, só dispara cron **uma vez por dia** — não serve
para post com hora marcada. O GitHub Actions dispara a cada 5 minutos de
graça, e é isso que o fluxo em `.github/workflows/agendador.yml` faz.

A senha fica no segredo `CRON_TOKEN` do repositório; ela não está em lugar
nenhum do código.

Atenção: o GitHub desliga fluxos agendados em repositório parado há 60 dias.
Se isso acontecer, é só abrir Actions e reativar.
