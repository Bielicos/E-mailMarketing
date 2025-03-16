<h1 align="center"> Projeto de E-mail Marketing </h1>

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) <br/> ![E-mail Marketing](https://img.shields.io/badge/E--mail%20Marketing-green?logo=gmail&logoColor=white) 

## Descrição 

Este projeto é um template de e-mail responsivo desenvolvido para criar mensagens de marketing ou notificações de cadastro para uma empresa fictícia chamada "Circle".

O código possui a versão "standard.html" com CSS padrão e sem restrições de tecnologias, que foi criado para facilitar a construção da versão "inline.html" onde utilizei das melhores práticas de CSS inline para fazer com que o código seja compatível com a maioria dos clientes de e-mail.

Criei este projeto open source com o intuito de aprender a fazer e-mail marketing na prática, onde foquei em acessibilidade a diversos clientes de e-mail, responsividade, código fácil de se entender e um template visualmente atraente.

## Instrução de Instalação

Verifique se o nodeJs está instalado, caso não esteja vá no [site oficial do Node.js](https://nodejs.org/) para fazer o download.

```bash
node -v
```

Instale as dependências

```bash
npm i
```


## Instrução de uso

Após baixar os pré requisitos, siga as instruções abaixo para realizar o teste :

1: Crie uma conta de teste ethereal clicando no botão "Create Ethereal Account" no [site oficial do Ethereal](https://ethereal.email/)

2 : Pegue o username e o pass, depois execute o comando "node sendEmail.js username pass" como no exemplo abaixo :

```bash
node sendEmail.js rickey.shanahan@ethereal.email QcQBsZT1TtsQjydnm9
```

3 : Após a execução, será exibido um link do Ethereal no terminal. Acesse esse link para visualizar o template de e-mail. Você pode testar o acesso por diferentes dispositivos para avaliar a responsividade.

## Contribuição

Ao enviar um pull request, você concorda em que sua contribuição estará sujeita aos termos da [licença MIT](LICENSE.txt).

## Gitflow

Criei padrões para tornar este código o mais limpo possível ao mesmo tempo em que ele seja responsível a maioria dos clientes de e-mail, é opcional segui-lo.

1) O gap entre os elementos será a partir de margin-top, dessa forma :

html
<!-- start margin 80px -->
<table class="margin1" style="border-collapse: collapse; border-spacing: 0;" cellspacing="0" cellpadding="0">
    <tr>
        <td height="80px" style="line-height: 80px; font-size: 0;">&nbsp;</td>                        
    </tr>
</table>
<!-- end margin 80px -->


2) Cada "container" deve ser especificado a partir de quando começa ( start ) e quando termina ( end ), como visto no exemplo acima.

3) A partir da criação de uma tag "Table", você deve aplicar as seguintes tags :

```html
<table class="margin1" style="border-collapse: collapse; border-spacing: 0;" cellspacing="0" cellpadding="0">
```

Esses dois atributos + essas duas estilizações removem o padding interno do table e o espaçamento entre as bordas que a tag table possui. Dessa forma, a tag "Table", literalmente se torna uma div com display grid onde você decide quantas colunas (td) e quantas linhas (tr) se tem cada conteiner (table). Porém, tenha atenção, visto que o border-collapse: collapse remove o padding, então quando precisar usar padding, remova-o.