MARKDOWN E YAML
[MARKDOWN_YAML.pdf](https://github.com/user-attachments/files/26583097/MARKDOWN_YAML.pdf)


PROMPT TÉCNICO E UNIVERSITÁRIO
[PROMPT.pdf](https://github.com/user-attachments/files/26583198/PROMPT.pdf)

SCRIPT LISTA
def calcular_media(lista):
    """
    Calcula a média de uma lista de números.
    
    Parâmetros:
        lista (list): Lista de números (int ou float)
    
    Retorna:
        float: Média dos valores
    
    Levanta:
        ValueError: Se a lista estiver vazia
        TypeError: Se houver elementos não numéricos
    """
    
    # Verifica se a lista está vazia
    if not lista:
        raise ValueError("A lista não pode estar vazia.")
    
    # Verifica se todos os elementos são números
    for item in lista:
        if not isinstance(item, (int, float)):
            raise TypeError("Todos os elementos devem ser números.")
    
    # Calcula a soma dos elementos
    soma = sum(lista)
    
    # Calcula a quantidade de elementos
    quantidade = len(lista)
    
    # Calcula a média
    media = soma / quantidade
    
    return media


# 🔍 Casos de teste

# Caso 1: Lista normal
print(calcular_media([10, 20, 30]))  # Saída esperada: 20.0

# Caso 2: Lista com números decimais
print(calcular_media([1.5, 2.5, 3.5]))  # Saída esperada: 2.5

# Caso 3: Lista vazia (erro esperado)
try:
    print(calcular_media([]))
except ValueError as e:
    print(e)  # Saída esperada: "A lista não pode estar vazia."
