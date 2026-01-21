🔍 Azure AI Search: Mineração de Dados em Cardápios
Este projeto foi desenvolvido como parte de um laboratório de Inteligência Artificial na Nuvem, onde utilizei o Azure AI Search para criar uma solução de Mineração de Conhecimento (Knowledge Mining). O objetivo foi transformar dados brutos de cardápios de diferentes restaurantes em uma base de dados pesquisável e inteligente.

🛠️ Tecnologias Utilizadas
Azure AI Search: Motor principal de busca e indexação.

Azure Blob Storage: Armazenamento dos arquivos brutos (PDFs e Planilhas).

Azure AI Services: OCR e Extração de Frases-chave (Key Phrases).

Linguagem de Consulta OData: Para filtragem e ordenação dos resultados.

🏗️ Arquitetura do Projeto
O fluxo de dados seguiu as etapas de Ingestão, Enriquecimento e Exploração:

Ingestão de Dados: Subi 4 arquivos de cardápios (Restaurantes: Bilu, FOX, Deoclécio e Juninho) em um contêiner no Azure Blob Storage.

Enriquecimento por IA (Skillset): * Utilizeis habilidades de IA para "ler" os arquivos.

Extraí entidades (como nomes de pratos) e frases-chave (ingredientes e preços).

Configurei o reconhecimento de idiomas e localidade.

Indexação: O indexador automatizou a leitura dos dados e mapeou as informações extraídas para um índice estruturado.

Exploração (Busca Semântica): Ativei o classificador semântico para que a busca não fosse apenas por palavras exatas, mas por contexto e relevância.

🚀 Resultados
Ao final do projeto, gerei um Aplicativo de Demonstração Web (HTML) que permite:

Pesquisar por ingredientes (ex: "Bacon", "Suco").

Filtrar por restaurante através de facetas na barra lateral.

Visualizar a pontuação de relevância de cada item (@search.rerankerScore).

📊 Insights Técnicos (O que aprendi)
O processo de consulta segue 4 estágios: Análise da consulta, análise lexical, recuperação de documento e pontuação.

O parâmetro $orderby é essencial para classificar os resultados.

O uso de Skillsets permite transformar dados não estruturados (textos em imagens/PDF) em dados estruturados (JSON).

💡 Como utilizar
Abra o arquivo index.html em qualquer navegador.

Utilize a barra de pesquisa para encontrar itens nos cardápios.

Use os filtros laterais para refinar a busca por categorias extraídas pela IA.