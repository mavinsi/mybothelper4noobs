# 🧾 Como um comando é estruturado?
Antes de aprendermos a criar um comando, vamos entender a sua estruturação, abaixo temos um comando simples que ao bot receber a mensagem ``hello`` ele ira responde-la com ``hello world``

```js
module.exports= {
    name: 'hello',
    description: 'simples hello world message',
    execute(message,args){

      // tudo que estiver aqui dentro sera executado!

        message.channel.send(`Hello world!`)
    }
}
```

o paramêtro ``name: ' '`` , define como vai ser chamado o comando, então caso quisessemos criar uma comando que é chamado por ``!log`` devemos adicionar essa string ao paramêtro como veremos abaixo


```js
module.exports= {
    name: '!log',
    ...
```
o proximo paramêtro é o ``description: ' '`` que é basicamente a descrição do comando, ele não possui nenhuma função além da organização... então vamos organizar né?

a proposta do nosso comando ``log`` é fazer o bot escrever no nosso terminal uma mensagem quando receber esse comando:

```js
module.exports= {
    name: '!log',
    description: 'faz o bot falar algo quando ser chamado por esse comando',
    ...
```

## 🏗️ Como criar seu proprio comando (simples)

agora vamos passar para execução do nosso comando para isso deveremos ter em mente que tudo que se encontra entre as chaves da função ``execute`` será executado caso o bot receba uma mensagem possuindo o prefixo declarado em ``name``.

então vamos tentar por em pratica oque descidimos na nossa descrição do comando, para isso vamos utilizar a função ``console.log()`` você pode aprender mais sobre essa função e outras no repositorio 4noobs de javascript: [CLIQUE AQUI](https://github.com/ThiagoDellaNoce/javascript4noobs) , vamos agora fazer o bot responder com um simples ``ola dev!``

```js
module.exports= {
    name: '!log',
    description: 'faz o bot falar algo quando ser chamado por esse comando',
    execute(){

      

        console.log(`ola dev!`)
    }
}
```

agora após ter terminado de desenvolver seu comando crie um arquivo em javascript e coloque na pasta /cmds/ para ele ser lido como um comando, vamos dar o nome de ``meucomando.js``, agora deveremos iniciar nosso bot com ``npm start`` como foi ensinado em [📥 Instalando & configurando](https://github.com/mavinsi/mybothelper4noobs/blob/main/roadmap/h_install.md), e agora vamos enviar uma mensagem para o bot de acordo com oque declaramos em ``name`` no caso ``!log``, se tudo estiver certo iremos receber no terminal a seguinte mensagem: 

```bash
...

[BOT] Executing meucomando.js command
ola dev!

```

E pronto parabéns você acabou de desenvolver seu primeiro comando para o MyBotHelper

<hr>

<h1 align="center">🎉 Por enquanto nossa aventura termina aqui, mas logo logo receberemos mais tutorias e documentação, muito obrigado por experimentar!🎉</h1>


