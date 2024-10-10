# ponderada_semana_9

Este repositório contém o código da API em Go e os scripts de teste de carga e stress usando a ferramenta k6. A API alvo dos testes está no arquivo `main.go`, enquanto os testes são definidos em diversos scripts JavaScript localizados na pasta `tests/`.

## Estrutura do Repositório

- **main.go**: Código da API alvo dos testes de carga e stress.
- **/tests**: Contém os scripts de teste do k6 escritos em JavaScript, incluindo testes de smoke, carga, stress, e pico.



## 1. Criar o Repositório

Foi criado um repositório no GitHub para armazenar os códigos do tutorial, com a seguinte estrutura de pastas:

- `main.go`: Código da API.
- `tests/`: Scripts de teste do k6.

## 2. Documentação das Execuções de Testes

Cada script de teste de carga foi executado usando o k6. Abaixo estão exemplos de execução de alguns testes:

### Exemplo 1: Teste Smoke
```bash
k6 run tests/smoke-test.js
```

### Exemplo 2: Teste de Carga
```bash
k6 run tests/load-test.js
```

### Exemplo 3: Teste de Stress
```bash
k6 run tests/stress-test.js
```

### Exemplo 4: Teste de Pico
```bash
k6 run tests/spike-test.js
```

Para executar esses testes localmente, siga as instruções:

1. Instale o k6: 
   ```bash
   brew install k6
   ```

2. Execute o script de teste desejado:
   ```bash
   k6 run tests/<script-de-teste>.js
   ```

3. Verifique a saída no terminal para visualizar os resultados.

---

## 3. Técnicas de TDD em Testes de Carga

Neste repositório, foram aplicadas as seguintes técnicas de TDD:

- **Design de Casos de Teste**: Os scripts de teste foram escritos com base nas expectativas de carga para a aplicação. Antes de desenvolver a API, esses testes ajudam a definir o comportamento esperado.
  
- **Ciclo Contínuo de Feedback**: À medida que o desenvolvimento avança, os testes são executados continuamente. O k6 pode ser integrado a pipelines de CI/CD, tornando-o ideal para uma abordagem de TDD.

- **Refatoração Baseada em Métricas**: Após a execução dos testes, o código é refatorado com base nas métricas coletadas para garantir que a aplicação atenda aos requisitos de desempenho.

---

## Como Usar

1. Clone o repositório:
   ```bash
   git clone <repository-url>
   ```

2. Navegue até a pasta `tests` e execute os testes de carga:
   ```bash
   cd tests
   k6 run <nome-do-script.js>
   ```

3. Confira os resultados diretamente no terminal após a execução dos testes.


## Conclusão

Este repositório não apenas segue os passos do tutorial de testes de carga usando k6, mas também aplica técnicas de TDD para garantir que a aplicação seja capaz de suportar diferentes cenários de carga e stress com performance aceitável.
