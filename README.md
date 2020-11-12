Instação do Mautic via docker-compose

#### O que é tratado neste docker-compose.yml:

* Configuração de contêineres mysql e mautic
* Configuração do contêiner nginx com configuração vhost personalizada (nginx.conf)
* Criação automática de cetificado self-signed

#### Como usar:

1. run ```docker-compose up``` neste diretório
2. adicione esta linha ao seu /etc/hosts file ```127.0.4.123 mautic.local```
3. acesse https://mautic.local
4. adicione o certificado apresentado a uma lista de certificados confiáveis ​​em seu navegador (o certificado é um certificado autoassinado criado na primeira execução deste exemplo)
5. passe pela configuração do Mautic (preencha `` `mauticdbpass``` como senha do mysql na página de configuração do banco de dados
6. teste o Mautic

#### Notas
* O certificado deve ser confiável. Pode não ser suficiente apenas clicar através do aviso em alguns navegadores.
* O mapeamento de hosts é necessário para tornar o certificado confiável (o nome deve corresponder ao CN do certificado).
* Se você deseja acessar o contêiner da máquina remota, deve substituir 127.0.4.123 pelo endereço do host docker.
