## Laboratório de integração entre spring boot, kafka e mysql

<p align="center">
  <img height="300" src="./imagem.png">
</p>

## Objetivos
- [x] Subir o apache kafka versão da confluent via docker-compose;
- [ ] Criar um projeto para produzir uma mensagem no tópico `meu-topico` do objeto `Pessoa`;
  - Atributos da classe `Pessoa`
  ```java
  public class Pessoa {
    private Long id;
    private String nome;
    private TipoDocumento tipo; //enum
    private String documento;
    //getter e setter
  }
  ```
- [ ] Criar um projeto para receber uma mensagem do tópico `meu-topico` do ojeto `Pessoa`;
- [ ] Subir um mysql via docker-compose;
- [ ] Gerar um connector do mysql no kafka;
- [ ] No projeto receptor logar os eventos via das operações de crud do mysql.

## :bulb: Orientações
- O modelo base para levantamento do kafka retirado do repositório padrão do [confluentinc](https://github.com/confluentinc/cp-all-in-one/blob/6.0.1-post/cp-all-in-one/docker-compose.yml);
- Para utilizar o docker compose no `mac` ou `windows` se faz necessário aumentar o alocamento de memória do docker para 8GB. `Preferences > Resouces > Advanced`;
- Para instalar o connector do mysql no kafka:
    - ```bash
       > docker exec -it connect bash
       ```
    - ```bash
       > confluent-hub install debezium/debezium-connector-mysql:1.3.1
      ```
