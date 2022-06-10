
## 🪄 Como funcionam os eventos?

Os eventos localizados na pasta ``/cmds/events``, são basicamente ações que são executados quando algum evento como um membro entrar ou sair do servidor ou alguém enviar mensagem na DM do bot, sim os comandos ``/cmds/`` são eventos também porém a diferença é que os comandos são eventos que são ativados quando o bot recebe uma mensagem com o um prefixo especifico já os eventos são quando ocorre eventos além de mensagens geralmente eventos em relação ao servidor como exemplificado acima.

## 💡 Como utilizar os eventos?

Vamos começar analisando um evento que já está presente no reposítorio do mybothelper, ele é o new_member esse evento é executado toda vez que um membro novo entra em qualquer servidor que o bot esteja:

```javascript
const mbhMain = require('../../index.js');
const version = require('../../package.json').version;

module.exports = {
  name: 'new_member',
  description:
    'this command is executed every time a member joins any server the bot is on',
  execute(client, member) {
    

  },
};
```

Como aprendemos anteriormente em [🧾 Como um comando é estruturado?](https://github.com/mavinsi/mybothelper4noobs/blob/main/roadmap/s1_command.md) , sabemos que tudo que estiver entre a função execute será executado quando comando ser solicitado, então como exemplo vamos fazer o bot nos notificar no terminal qual nome da pessoa que entrou no servidor, para isso vamos utilizar um console.log novamente e iremos usar o paramêtro member para adquirir as informações necessarias (no caso o nome) do membro que entrou no servidor para isso utilizaremos ``member.user.username`` (pegamos do member as informações de usuario e dessas informações de usuarios pegamos o username), e agora simplesmente vamos coloca-los dentro do console.log ficando assim:
```javascript
const mbhMain = require('../../index.js');
const version = require('../../package.json').version;

module.exports = {
  name: 'new_member',
  description:
    'this command is executed every time a member joins any server the bot is on',
  execute(client, member) {
  console.log(member.user.username + " Entrou no servidor")
  },
};
```

se tudo estiver certo nós teremos o seguindo resultado no terminal:


```bash
...

John doe entrou no servidor 


```

<h1 align="center">🎉 Por enquanto nossa aventura termina aqui, mas logo logo receberemos mais tutorias e documentação, muito obrigado por experimentar!🎉</h1>



