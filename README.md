# Projeto-Final-IA

Este projeto tem como objetivo a aplicação prática de técnicas de Inteligência Artificial baseadas em Redes Neurais Convolucionais (CNN) para o desenvolvimento de um sistema de detecção automática de pessoas em ambientes reais do Campus de Itapajé com foco em aplicações relacionadas à Segurança
da Informação, como monitoramento, controle de acesso e análise de ocupação de espaços.

Para a implementação, será utilizado o framework Detectron2, desenvolvido pelo Facebook AI Research, que disponibiliza modelos pré-treinados para tarefas de detecção e segmentação de objetos. O projeto não exige o treinamento de uma CNN do zero, mas sim a adaptação (fine-tuning) de um modelo pré-treinado para um conjunto de dados específico, contendo apenas a classe de interesse, no caso, pessoas.

Este trabalho propõe o desenvovimento de uma adaptação do modelo de Inteligência artificial Detectron2, o ambiente escolhido para sua aplicação é de salas da faculdade (sala de estudos, sala de projetos e salas de aula) para a função de detectar pessoas em salas da faculdade, retornando o número de pessoas na sala e os status dela, se a sala está ocupada ou vazia.

