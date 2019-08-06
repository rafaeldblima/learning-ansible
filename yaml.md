Comando para exibir o yaml formatado como dict:
python show_yaml_python.py

Exemplos:
# Várias maneiras de escrever string
    no_quotes: this is a string example\n
    double_quotes: "this is a string example\n"
    single_quotes: 'this is a string example\n'

# Linhas multiplas
    example_key_1: |
    this is a string
    that goes over
    multiple lines

# Linhas multiplas juntas em uma só com \n no final
    example_key_1: >
    this is a string
    that goes over
    multiple lines

# Linhas multiplas juntas em uma só
    example_key_1: >-
    this is a string
    that goes over
    multiple lines

# Diversas maneiras de representar boolean
   # false, False, FALSE, no, No, NO, off, Off, OFF
    # true, True, TRUE, yes, Yes, YES, on, On, ON

# Lista
    - item 1
    - item 2
    - item 3
    - item 4
    - item 5

# Lista de objetos
    - example_1: 
        - item_1
        - item_2
        - item_3

    - example_2: 
        - item_4
        - item_5
        - item_6
