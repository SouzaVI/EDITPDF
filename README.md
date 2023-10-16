## 1. CONTEXTUALIZAÇÃO


O surgimento do Plugin foi uma resposta à crescente demanda por uma solução eficiente na realização de laudos de amostras em formato PDF. Muitos profissionais e organizações que lidam com análise de dados e informações precisavam adicionar informações específicas, como o nome de talhões associados a amostras correspondentes, bem como a capacidade de identificar e selecionar os maiores ou menores valores de atributos em um conjunto de dados.

Antes da introdução desse Plugin, o processo de realizar essas tarefas era predominantemente manual, o que frequentemente se revelava demorado e suscetível a erros humanos. A necessidade de otimização e automação dessas ações tornou-se cada vez mais evidente, uma vez que a eficiência e a precisão são cruciais em tarefas de análise de dados.

O Plugin, portanto, foi desenvolvido para atender a essa necessidade específica. Ele permite aos usuários importar amostras de PDF e, de forma simplificada e automatizada, adicionar os nomes de talhões correspondentes. Além disso, oferece uma funcionalidade para selecionar automaticamente os maiores ou menores valores dos atributos, simplificando significativamente o processo de geração de laudos.

Essa automação não apenas economiza tempo, mas também minimiza erros, tornando o processo de laudo de amostras em PDF mais eficiente e confiável. O Plugin é uma solução valiosa para aqueles que dependem da análise de dados e relatórios precisos em seu trabalho, proporcionando uma maneira mais eficaz de lidar com amostras em PDF e melhorar a produtividade.


## 2. USO DO PLUG IN EDITOR PDF 
O plugin foi criado especificamente para o QGIS 3.28 e versões posteriores. Cada aspecto da interface, funcionalidades e demais recursos foi meticulosamente projetado para efetivamente melhorar o processo de edição do Laudo Exata e IBRA

### 2.1 Pré - Requisitos
   #### 2.1.1 Caminho de pastas
No disco C:/, é necessário criar as seguintes pastas:

Disco C:

 `1. geoprocessamento`

  `1.1 assets`

Na pasta assets  será armazenado arquivo **fundo_exata.pdf** o arquivo encontra-se na pasta de aplicativos do geoprocessamento.   

#### 2.1.2 Instalação das dependências e instalação do Plugin no Qgis
No ambiente OSgeo4W instale os seguintes pacotes:

`python -m pip install PyPDF2`

`python -m pip install reportlab`

`python -m pip install XlsxWriter`

No qgis ir em complementos  e instale a partir de um zip a versão do plug in mais atualizada

### 2.2 Apresentação da tela
Após a instalação do plug-in, você o encontrará na barra de ferramentas, onde seu ícone é semelhante ao de um computador. Se você não visualizar o ícone, pode ser necessário habilitar o plug-in. Para fazer isso, vá até a seção de complementos, selecione "Gerenciar e instalar complementos", vá para a guia "Instalados" e ative o plug-in chamado **Edição de Análise**.

![habilitar](https://github.com/SouzaVI/EDITPDF/assets/98165012/bc209f62-1bb1-44d2-9293-5894d6857813)


> **1. Importe o contorno da fazenda, que deve estar previamente carregado no software QGIS.**

> **2. Selecione o modelo em PDF que servirá como base para criar o novo laudo editado. O modelo está localizado na pasta de aplicativos.**

> **3. Importe os pontos da fazenda, os quais também devem estar previamente carregados no QGIS.**

> **4. Importe o arquivo Excel do laudo, que é gerado a partir da conversão do PDF.**

> **5. Utilize a caixa de seleção para configurar o seu laudo de acordo com suas preferências.**

> **6. Se optar pela análise parcial, escolha a quantidade de amostras que deseja incluir no laudo.**

> **7. Exporte o laudo editado para download.**

![tela_plugin](https://github.com/SouzaVI/EDITPDF/assets/98165012/2adf8582-47ed-4a4c-92dd-699d3192dedf)

## 3. PROCEDEMENTO  EM VIDEO DE INSTALAÇÃO DE REQUISITOS E USO DO PLUG IN

### 3.1 Pré - Requisitos

https://github.com/SouzaVI/EDITPDF/assets/98165012/e834e614-4d56-4c7d-8f67-02bd4415be68

### 3.2 Uso do Plug in

Devido ao tamanho do vídeo, o tutorial foi hospedado no google drive:

[Uso do Plug in Editor de PDF](https://drive.google.com/open?id=1qbhfdyfQgZ90kD2Hi_QLZqdinn6P0L0p&usp=drive_fs)

## 4. INFORMAÇÕES IMPORTANTE

A função é altamente adaptável, permitindo que você gere um laudo em formato PDF de forma parcial, sem a necessidade de ativar as opções da caixa de seleção. Nesse caso, basta ter o arquivo Excel preparado de acordo com suas necessidades, respeitando todos os requisitos dos nomes de colunas de cada laboratório.

Este plugin possui uma versão disponível no formato de um Jupyter notebook de forma separado para cada laboratório. Isso significa que, além da funcionalidade padrão, você tem a opção de usar o plugin diretamente em um ambiente Jupyter notebook, o que pode ser especialmente útil para aqueles que estão familiarizados com o ecossistema Python e desejam incorporar essa funcionalidade em seus fluxos de trabalho. Essa versão no Jupyter notebook permite uma integração mais flexível e personalizada, oferecendo um conjunto de ferramentas e recursos que podem ser adaptados às suas necessidades específicas. Isso adiciona uma camada adicional de versatilidade ao plugin, tornando-o uma opção atraente para uma variedade de usuários e cenários de uso.

## 5. BUG (PROBLEMA NÃO SOLUCIONADO)

### 5.1 Erro de índice fora do comprimento (IndexError) 

Se você precisar criar um laudo Exato com apenas 2 páginas (que incluam 8 amostras e a contracapa), será necessário criar dados fictícios para totalizar 9 amostras. Após a geração do laudo PDF editado, você poderá remover esses dados fictícios.

