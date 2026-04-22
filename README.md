# validator_br

Biblioteca em Python para validação de CPF.

Implementa a validação completa com base no cálculo dos dígitos verificadores, incluindo normalização da entrada e rejeição de sequências inválidas.

---

## Instalação

Distribuição via GitHub:

```bash
pip install git+https://github.com/CodeTangent/validator_br.git
```

---

## Uso

### Importação (versão atual)

```python
from validator_br.cpf import CPF
```

> Observação: na versão 2.0 a importação será simplificada para:
>
> ```python
> from validator_br import CPF
> ```

---

### Exemplo básico

```python
from validator_br.cpf import CPF

cpf = CPF("529.982.247-25")

if cpf.is_valid():
    print("CPF válido")
else:
    print("CPF inválido")
```

---

### Uso direto

```python
from validator_br.cpf import CPF

print(CPF("111.111.111-11").is_valid())  # False
print(CPF("52998224725").is_valid())    # True
```

---

## Comportamento

A classe realiza automaticamente:

* Remoção de caracteres não numéricos
* Validação de tamanho (11 dígitos)
* Rejeição de sequências repetidas
* Cálculo dos dois dígitos verificadores

A entrada pode ser fornecida com ou sem formatação.

---

## API

### Classe `CPF`

#### Inicialização

```python
CPF(raw_cpf)
```

**Parâmetros**

* `raw_cpf` (str | int): valor do CPF em qualquer formato

---

#### Método `is_valid`

```python
cpf.is_valid()
```

**Retorno**

* `True` se o CPF for válido
* `False` caso contrário

---

## Requisitos

* Python >= 3.8

---

## Roadmap

* Simplificação da importação
* Organização interna do pacote
* Suporte a CNPJ
* Funções auxiliares (ex: formatação)

---

## Testes

Não incluídos nesta versão inicial.

---

## Licença

MIT

---

## Autor

CodeTangent

Email: [developercsharp14@gmail.com](mailto:developercsharp14@gmail.com)
