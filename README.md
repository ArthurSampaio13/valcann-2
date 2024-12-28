# Funcionamento da Pipeline
### Trigger do Workflow:

A pipeline é acionada sempre que há um push nas branches main (produção) ou develop (homologação).
### Processo de Build:

O GitHub Actions realiza o empacotamento dos componentes frontend e backend.
### Execução de Testes:

São executados testes automatizados para assegurar que o código está funcionando corretamente.
###  Deploy Automatizado:

Após a aprovação nos testes, a aplicação é automaticamente implantada no ambiente de homologação.
Uma vez validada a homologação, a mesma versão é promovida para produção sem intervenção manual.
### Monitoramento e Notificações:

Utiliza AWS CloudWatch para monitorar o status dos deploys.
Notificações são enviadas via Slack ou email para informar sobre o sucesso ou falha dos deploys.