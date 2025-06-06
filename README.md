
# 🗺️ Sistema de Relato de Catástrofes
Contruimos um  sistema de linha de comando(CLI) para relato de catastrofes. que devem estar dentro de um raio de 10km a partir do ponto de referência informado pelo usuário.

# Autores
- André Eduardo Martins  - 563297
- Felipe Hui             - 565169
- Rafael Vaz de Lima     - 566429 

# Caracteristicas técnicas
- Utilizamos arrays dinâmicos para gerenciar a memória de forma eficiente, ja que o número de relatores e relatos é desconhecido antecipadamente e deve responder a necessidade em tempo de execução.
- Organizamos nossos itens em structures, e utilizamos ponteiros para alocação e atribuições.
- Priorizamos a manutenibilidade e simplicidade com base no nosso conhecimento atual.
- A linguagem para desenvolvimento do código escolhida por nós foi C.

# Funcionalidades

- Definir um **ponto central de referência** para controle de relatos por proximidade.
- **Cadastrar relatores**, com dados como nome, documento (CPF), e-mail e endereço.
- **Registrar relatos de catástrofes** com:
  - Tipo da catástrofe
  - Descrição
  - Data e hora do evento
  - Localização (latitude e longitude)
- Funções de query:
  - listar todos relatos catastrofes.
  - **Buscar relatos por tipo** de catástrofe.
  - **Buscar relatos por localização geográfica** (dentro de um raio definido).
  - **Buscar relatos por período** (intervalo de datas e horas).
- Validação automática para:
  - Formatos de data/hora
  - Distância dentro do raio máximo (10 km por padrão)
  - Existência de relator
  - Consistência de dados

#  Estrutura do Código

O projeto é modular e organizado com o uso de `structs` para:

- `Relator`: dados dos usuários que registram eventos
- `Relato`: dados detalhados do evento
- `Coordenadas`: estrutura de latitude/longitude
- Funções auxiliares para manipulação de strings, datas, localização e memória

#  Cálculo de Distância

Utilizamos a fórmula **Haversine** para calcular a distância geodésica entre dois pontos (latitude/longitude), permitindo determinar se o relato está dentro da área de interesse (10 km do ponto central).

#  Requisitos

- Compilador C compatível com C99 ou superior
- Sistema operacional com suporte a biblioteca padrão (`stdio.h`, `stdlib.h`, `string.h`, `math.h`, `time.h`)

