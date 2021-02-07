# DONT ASK TO ASK

> Primeiramente de tudo, veja [dontasktoask] e [xyproblem] para entender um pouco mais.

### Trechos de código
Quando você enviar um trecho de código, certifique-se de enviar todas as partes importantes onde esse código está sendo executado, como funções que ele consome, váriaveis declaradas...

Também tente esclarecer o máximo possível sobre que você realmente quer fazer, pois não temos bolas de cristal.

_Exemplo:_

**usuário anônimo** meu código não funciona e eu não sei porque
  ```java
  final Gamer gamer = GamerRegistry.get(player);
  double coins = gamer.getCoins();

  gamer.sendMessage("Seus coins: %s", coins); 
  ```
**zkingboos** o quê o player é? O quê `GamerRegistry.get(player)` faz? Os coins estão sendo retornados de maneira correta? Ele está salvo nesse registro?

<br/>

> Ao invés de mandar apenas o trecho código, você pode declarar mais especiamente sobre o quê é:

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
  porém fiz um código e não funcionou, queria saber qual pode ser a causa disso.
  ```java
  final Gamer gamer = GamerRegistry.get(player);
  double coins = gamer.getCoins();

  gamer.sendMessage("Seus coins: %s", coins); 
  ```

Nunca tenha medo de perguntar sobre algo, pois ninguém nunca nasceu sabendo.

[dontasktoask]: https://dontasktoask.com
[xyproblem]: https://xyproblem.info/
