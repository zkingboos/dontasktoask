> Primeiramente de tudo, veja [dontasktoask] e [xyproblem] para entender um pouco mais.

### Trechos de código
Quando você enviar um trecho de código, certifique-se de enviar todas as partes importantes onde esse código está sendo executado, como funções que ele consome, váriaveis declaradas...

Também tente esclarecer o máximo possível sobre que você realmente quer fazer, pois não temos bolas de cristal.

_Exemplo:_

**usuário anônimo** meu código não funciona e eu não sei porque
  ```java
  public onCommand(CommandSender sender, Command command, String label, String[] args){
    Player player = (Player) sender;

    final Gamer gamer = GamerRegistry.get(player);
    double coins = gamer.getCoins();

    gamer.sendMessage("Seus coins: %s", coins); 
  }
  ```
**zkingboos** O que `GamerRegistry.get(player)` faz? Os coins estão sendo retornados da maneira correta? Ele está salvo nesse registro?

<br/>

> Ao invés de mandar apenas o trecho código, você pode declarar mais especificamente sobre o que é:

**usuário anônimo** Eu tenho uma classe de registro chamado GamerRegistry, onde contém todos os jogadores salvos no cache que são salvos quando entram no servidor, todos os dados deles são obtidos atráves do banco de dados. A estrutura da classe Gamer é essa:
  ```java
  public class Gamer {
    private Player player;
    private double coins;
  }
  ```
a classe onde eu obtenho todos os dados que preciso:
  ```java
  public class GamerDAO {
      //some code..
  }
  ```
porém fiz esse código e não funcionou, queria saber qual pode ser a causa disso.
  ```java
  public onCommand(CommandSender sender, Command command, String label, String[] args){
    Player player = (Player) sender;

    final Gamer gamer = GamerRegistry.get(player);
    double coins = gamer.getCoins(); //coins = 0

    gamer.sendMessage("Seus coins: %s", coins); 
  }
  ```
Já testei anteriormente, o jogador realmente existe dentro do registro mas os coins estão retornando 0 mesmo que eu defina eles pra algum valor

<br/>

Nunca tenha medo de perguntar sobre algo, pois ninguém nunca nasceu sabendo.

[dontasktoask]: https://dontasktoask.com
[xyproblem]: https://xyproblem.info/
