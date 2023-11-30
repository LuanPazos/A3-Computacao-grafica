# A3-Computacao-grafica
 Luan Carlos Machado

O arquivo Deve ser rodado com o google colab e realizar a substituição do caminho das imagens desejadas


## Introdução
Considerada a principal fonte de energia do mundo, a energia elétrica é um elemento essencial no cotidiano das pessoas. Manter hospitais funcionando, conservar alimentos, proporcionar iluminação pública, etc, tudo isso é possível através da energia elétrica. Garantir a qualidade da eletricidade é muito importante, então/por este motivo, falhas devem ser evitadas, de outro modo/caso contrário podem provocar danos a equipamentos e/ou pessoas e também provocar interrupções de energia elétrica. O local que distribui energia elétrica para as residências, comércios, hospitais, etc, é denominado/chamado/conhecido subestação. 
Uma subestação é uma instalação elétrica formada por um conjunto de equipamentos responsáveis pela transmissão e distribuição da energia. As subestações elétricas são um elemento imprescindível para o funcionamento de uma rede elétrica, por este motivo é necessário o monitoramento desses espaços para impedir o acesso de pessoas não autorizadas.
O objetivo principal desse projeto é desenvolver um sistema que detecta somente pessoas em uma imagem, vídeo ou câmera ao vivo/CTV/webcam, proporcionando a proteção desses locais.
sugestao de adicionar exemplos de aplicacao do projeto




## Projeto

Este relatório detalha o desenvolvimento de um projeto dedicado à identificação de pessoas em áreas com risco elétrico, empregando técnicas avançadas de Deep Learning. O foco principal é a utilização do YOLO (You Only Look Once) para o reconhecimento eficiente de ações humanas em vídeos de alta resolução, integrando o rastreamento. 
YOLO (You Only Look Once): Uma Visão Geral:
O YOLO é uma arquitetura de Deep Learning que se destaca por sua eficiência na detecção de objetos em tempo real. Diferentemente de abordagens convencionais, o YOLO examina a imagem como um todo em uma única passagem, o que o torna excepcionalmente rápido e eficaz. 
Como Funciona em Nosso Projeto:
O coração do projeto repousa na utilização do YOLO, uma arquitetura de rede neural otimizada para a detecção eficiente de objetos em imagens e vídeos em tempo real. O YOLO será empregado para identificar pessoas em áreas com risco elétrico, oferecendo uma abordagem ágil e precisa para a detecção de ações humanas.






Divisão da Imagem em Grades:

Antes da aplicação do YOLO, a imagem é subdividida em uma grade, onde cada célula é responsável por prever bounding boxes e probabilidades associadas a objetos dentro dessas caixas.

Predição de Bounding Boxes e Classes:

Cada célula da grade prevê várias bounding boxes, especificando parâmetros como coordenadas x e y do centro, largura, altura e a probabilidade de conter um objeto.
Para cada bounding box, são previstas probabilidades de pertencer a diferentes classes de objetos, destacando particularmente a classe "pessoa".

Supressão Não Máxima (Non-Maximum Suppression - NMS):

O algoritmo utiliza a técnica de NMS para reduzir redundâncias, mantendo apenas as bounding boxes mais confiantes e evitando detecções duplicadas.

Integração com OpenCV:

As detecções realizadas pelo YOLO são integradas ao fluxo do projeto através da biblioteca OpenCV.
O OpenCV processa os quadros do vídeo, extrai as informações das bounding boxes previstas pelo YOLO e exibe os resultados de maneira eficiente.
Ao seguir essa abordagem, o YOLO desempenha um papel central, oferecendo uma detecção robusta e em tempo real de pessoas, essencial para a implementação de medidas preventivas em áreas com risco elétrico.

Linguagem de Programação e Ambiente de Desenvolvimento:

A implementação deste projeto foi conduzida utilizando a linguagem de programação Python, conhecida por sua flexibilidade, vasta comunidade de desenvolvedores e bibliotecas ricas em recursos para ciência de dados e aprendizado de máquina.
O ambiente de desenvolvimento escolhido foi o Google Colab, uma plataforma baseada na nuvem que oferece acesso gratuito a recursos computacionais, incluindo GPUs, facilitando o treinamento de modelos de Deep Learning de maneira eficiente. O Google Colab é particularmente adequado para projetos que envolvem processamento intensivo de dados, como é o caso deste projeto de identificação de pessoas em áreas com risco elétrico.


Estruturas Essenciais: 
Darknet:
A estrutura Darknet é um framework dedicado ao YOLO (You Only Look Once). Essa estrutura fornece a arquitetura de rede neural necessária para treinar e executar modelos YOLO, incluindo a versão específica usada em nosso projeto. O Darknet é essencial para a aplicação eficiente do YOLO na detecção de objetos, como a identificação de pessoas em vídeos de alta resolução.

OpenCV (cv2):

A biblioteca OpenCV desempenha um papel crucial no processamento de imagem e vídeo. No projeto, é utilizada para a manipulação de quadros de vídeo, extração de características e a exibição dos resultados. As funções do OpenCV proporcionam uma base sólida para operações relacionadas à visão computacional.

Numpy:

NumPy é empregado para manipulação eficiente de arrays e operações matemáticas. Sua integração permite cálculos rápidos e eficazes nas informações extraídas dos quadros de vídeo.

Pillow (PIL):

O módulo Image do Pillow (PIL) é utilizado para operações de manipulação de imagens, incluindo carregamento, conversão de formatos e outras transformações necessárias durante o processamento.

IO:

O módulo io é essencial para operações de entrada/saída, especialmente na manipulação de imagens e dados provenientes de diferentes fontes.

HTML:
O uso do módulo HTML é relevante para a exibição de resultados e informações no ambiente Colab.

Time:

O módulo time é incorporado para medição de tempo durante o processamento, fornecendo insights sobre a eficiência do sistema.


Matplotlib:

A biblioteca Matplotlib é explorada para a geração de gráficos e visualização de dados, oferecendo uma representação visual das informações processadas.



## Resultados:

Os resultados obtidos durante a fase de testes e validação indicam um desempenho promissor do sistema. A detecção de pessoas em tempo real, juntamente com a capacidade de análise retrospectiva de vídeos, demonstrou eficácia na identificação de situações de risco elétrico. A taxa de precisão na detecção de pessoas atendeu às expectativas, e o sistema foi capaz de gerar o resultado de forma ágil e eficiente.

Ambientes Residenciais:
Os resultados visíveis na Figura 1 e Figura 2 ilustram a aplicação efetiva da ferramenta em um contexto residencial. A disposição da câmera em um ângulo estratégico possibilita uma visão abrangente de uma tomada específica. O foco central deste caso de estudo reside na detecção de presença de crianças em ambientes potencialmente perigosos, nos quais o risco de choque elétrico é eminentemente elevado. A abordagem proposta visa não apenas à identificação precoce da presença infantil, mas também à implementação de medidas de proteção destinadas a mitigar possíveis ameaças à segurança elétrica e, por consequência, resguardar o bem-estar das crianças.



Figura 1

https://static-2frt.mo.cloudinary.net/images/9f787fac60f9aea73f93.jpeg

Figura 2

https://s2.glbimg.com/rDED6CytTvbxuMM77Kou0kyQdl4=/620x453/e.glbimg.com/og/ed/f/original/2013/10/30/cf239prisocorros_1.jpg


Ambientes Externos:

No contexto da detecção de indivíduos em ambientes de risco elétrico, como centrais de energia, a implementação de um sistema de vigilância torna-se essencial para garantir a integridade e segurança dos trabalhadores e visitantes. A figuras 3 exemplificam a eficácia desta abordagem em um cenário específico.

A disposição estratégica das câmeras em ângulos que abrangem áreas críticas de uma central de energia permite a detecção precisa da presença humana. Este projeto visa não apenas à identificação de indivíduos em locais de risco elétrico, mas também à implementação de ações preventivas e corretivas em tempo real. A capacidade de identificar prontamente a presença de pessoas em áreas perigosas possibilita a ativação imediata de protocolos de segurança, incluindo evacuação ou restrição de acesso, minimizando assim os riscos de acidentes elétricos.

Figura 3 

https://www.4oito.com.br/media/noticias/Carlos-Moises-em-Sideropolis_41487.jpg


Dificuldades:

A Ferramenta apresentou dificuldades em detectar todos em um vídeo ou imagem que contenha um elevado número de pessoas, como representado na figura 4.





figura 4 

Este projeto tem como principal objetivo realizar a detecção de objetos em imagens estáticas e transmissões de vídeo ao vivo, integrando as poderosas ferramentas Darknet e OpenCV. Ao clonar o repositório Darknet e configurar o ambiente para utilizar GPU e OpenCV, o projeto viabiliza a detecção de objetos em tempo real.As funcionalidades abrangem desde a captura de fotos da webcam, processamento da imagem capturada utilizando Darknet para detecção de objetos, até a transmissão de vídeo ao vivo com sobreposição de caixas delimitadoras nas detecções. Além disso, o projeto possibilita o processamento de arquivos de vídeo gravados, integrando a detecção de objetos Darknet e gerando um novo vídeo de saída com uma taxa de quadros aumentada.Os resultados visuais, como imagens e vídeos, exibem detecções de objetos destacadas por caixas delimitadoras coloridas. Os usuários têm a facilidade de baixar os resultados, proporcionando uma experiência prática e flexível para experimentação em detecção de objetos.Essa aplicação é significativa em diversos cenários, incluindo segurança, automação e análise de tráfego. O projeto oferece uma estrutura adaptável para implementação de detecção de objetos, destacando-se por sua abordagem prática e eficaz em ambientes colaborativos, como o Google Colab.




## CONCLUSÃO
Nas considerações finais deste projeto, destaca-se a conquista relevante na aplicação prática de tecnologias avançadas para detecção de objetos. A integração bem-sucedida da arquitetura YOLO com o OpenCV resultou em um sistema robusto e eficiente, capaz de realizar detecções precisas e analisar retrospectivamente vídeos para identificação de padrões.
Os resultados obtidos durante os testes indicam uma eficácia promissora em nossos testes realizados. A capacidade do sistema em fornecer uma visão abrangente e detectar precocemente potenciais riscos, contribuindo significativamente para nossos resultados.
Entretanto, é importante reconhecer os desafios enfrentados, especialmente em situações com um elevado número de pessoas. Esses desafios fornecem insights valiosos para melhorias futuras, destacando a importância contínua da pesquisa e desenvolvimento nesta área.
A adaptação do sistema para diferentes situações e a flexibilidade para ajustes sugerem um potencial contínuo de inovação, mas também estabelece uma base sólida para avanços futuros e aplicações mais amplas na interseção da visão computacional.
Em conclusão, este projeto ilustra a relevância da aplicação de tecnologias avançadas em diversas áreas, A integração bem-sucedida da ferramenta como YOLO e OpenCV não apenas reflete avanços tecnológicos, mas também projeta um futuro em que a convergência entre visão computacional e segurança tornam-se cruciais para criar ambientes mais seguros e eficientes por meio da implementação prática da tecnologia.
