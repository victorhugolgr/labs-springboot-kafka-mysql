## Laboratório de integração entre spring boot, kafka e mysql

<p align="center">
  <img height="300" src="./imagem.png">
</p>

## Objetivos
- [ ] Subir o apache kafka versão da confluent via docker-compose;
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
