
# API de Validação de Dados

Esta API realiza validações básicas de dados, como validação de e-mail, número de telefone, CPF e verificação de número positivo.

## Como Usar

A API está acessível através de uma URL e utiliza os parâmetros via **GET** para realizar as validações.

### Exemplos de Uso

- **URL Base:**  
  `http://seudominio.com/api.php?action=validar_email&email=exemplo@dominio.com`

  **Nota:** Substitua `seudominio.com` pelo seu subdomínio ou endereço do servidor onde a API está hospedada.

## Métodos da API

### 1. Validar E-mail
- **Rota:** `/api.php?action=validar_email&email=<email>`
- **Parâmetros:**
  - `email` (obrigatório): O e-mail a ser validado.

- **Exemplo de Requisição:**  
  ```text
  GET /api.php?action=validar_email&email=exemplo@dominio.com
  ```

- **Resposta:**
  - Se válido:
    ```json
    {
      "acao": "validar_email",
      "email": "exemplo@dominio.com",
      "valido": true
    }
    ```
  - Se inválido:
    ```json
    {
      "acao": "validar_email",
      "email": "exemplo@dominio.com",
      "valido": false,
      "mensagem": "E-mail inválido."
    }
    ```

### 2. Validar Telefone
- **Rota:** `/api.php?action=validar_telefone&telefone=<telefone>`
- **Parâmetros:**
  - `telefone` (obrigatório): O número de telefone a ser validado.

- **Exemplo de Requisição:**  
  ```text
  GET /api.php?action=validar_telefone&telefone=999999999
  ```

- **Resposta:**
  - Se válido:
    ```json
    {
      "acao": "validar_telefone",
      "telefone": "999999999",
      "valido": true
    }
    ```
  - Se inválido:
    ```json
    {
      "acao": "validar_telefone",
      "telefone": "999999999",
      "valido": false,
      "mensagem": "Número de telefone inválido."
    }
    ```

### 3. Validar CPF
- **Rota:** `/api.php?action=validar_cpf&cpf=<cpf>`
- **Parâmetros:**
  - `cpf` (obrigatório): O CPF a ser validado.

- **Exemplo de Requisição:**  
  ```text
  GET /api.php?action=validar_cpf&cpf=12345678909
  ```

- **Resposta:**
  - Se válido:
    ```json
    {
      "acao": "validar_cpf",
      "cpf": "12345678909",
      "valido": true
    }
    ```
  - Se inválido:
    ```json
    {
      "acao": "validar_cpf",
      "cpf": "12345678909",
      "valido": false,
      "mensagem": "CPF inválido."
    }
    ```

### 4. Verificar Número Positivo
- **Rota:** `/api.php?action=numero_positivo&numero=<numero>`
- **Parâmetros:**
  - `numero` (obrigatório): O número a ser verificado.

- **Exemplo de Requisição:**  
  ```text
  GET /api.php?action=numero_positivo&numero=5
  ```

- **Resposta:**
  - Se o número for positivo:
    ```json
    {
      "acao": "numero_positivo",
      "numero": "5",
      "valido": true
    }
    ```
  - Se o número não for positivo:
    ```json
    {
      "acao": "numero_positivo",
      "numero": "-5",
      "valido": false,
      "mensagem": "Número não é positivo."
    }
    ```

## Como Testar

1. **Validar E-mail**:
   - Exemplo de URL para testar:
     ```text
     http://seudominio.com/api.php?action=validar_email&email=exemplo@dominio.com
     ```

2. **Validar Telefone**:
   - Exemplo de URL para testar:
     ```text
     http://seudominio.com/api.php?action=validar_telefone&telefone=999999999
     ```

3. **Validar CPF**:
   - Exemplo de URL para testar:
     ```text
     http://seudominio.com/api.php?action=validar_cpf&cpf=12345678909
     ```

4. **Verificar Número Positivo**:
   - Exemplo de URL para testar:
     ```text
     http://seudominio.com/api.php?action=numero_positivo&numero=5
     ```


Agora, sua API está configurada para validar e verificar dados como e-mail, telefone, CPF e números positivos. Basta fazer as requisições corretamente e você receberá a resposta correspondente.
