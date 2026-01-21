# Projeto-Final-IA

Este projeto tem como objetivo a aplicação prática de técnicas de Inteligência Artificial baseadas em Redes Neurais Convolucionais (CNN) para o desenvolvimento de um sistema de detecção automática de pessoas em ambientes reais do Campus de Itapajé com foco em aplicações relacionadas à Segurança
da Informação, como monitoramento, controle de acesso e análise de ocupação de espaços.

Para a implementação, será utilizado o framework Detectron2, desenvolvido pelo Facebook AI Research, que disponibiliza modelos pré-treinados para tarefas de detecção e segmentação de objetos. O projeto não exige o treinamento de uma CNN do zero, mas sim a adaptação (fine-tuning) de um modelo pré-treinado para um conjunto de dados específico, contendo apenas a classe de interesse, no caso, pessoas.

# O projeto foi desenvolvido e executado utilizando:

- Google Colab com GPU
- Python 3.10+
- PyTorch com CUDA
- Detectron2
- OpenCV
- Roboflow (para anotação das imagens)
- Formato de dataset: **COCO JSON**

Este trabalho propõe o desenvovimento de uma adaptação do modelo de Inteligência artificial Detectron2, o ambiente escolhido para sua aplicação é de salas da faculdade (sala de estudos, sala de projetos e salas de aula) para a função de detectar pessoas em salas da faculdade, retornando o número de pessoas na sala e os status dela, se a sala está ocupada ou vazia.

# O projeto foi estruturado da seguinte forma:

data/
├── images/
├── annotations/

training/
├── train.py

inference/
├── test_model.py

utils/
├── dataset_utils.py

results/
├── metrics/
├── images/

main.py
README.md
requirements.txt

# Passo a passo para execução

### 1. Preparar o ambiente
No Google Colab, ativar a GPU em:
  Runtime → Change runtime type → Hardware Accelerator → GPU

  
### 2.Instalar dependências:
```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
pip install 'git+https://github.com/facebookresearch/detectron2.git'
pip install opencv-python
```
### 3. Organizar o dataset
As imagens do campus e os arquivos de anotação no formato COCO JSON devem ser colocados em:
data/images/
data/annotations/_annotations.coco.json

### 4. Treinar o modelo
Execute:
python training/train.py
O modelo treinado será salvo em:
training/output/model_final.pth

### 5. Executar inferência e métricas

python inference/test_model.py

# Exemplos de Resultados

![Detecção de Sala ocupada](results/images/ocp.jpg)

![Detecção de Sala Vazia](results/images/vz.jpg)

# Aplicação em Segurança da Informação

A aplicação desse trabalho na área de segurança da informação pode ser aproveitado para proteção de ambientes fisicos, onde estão localizados os ativos, e uma gestão de áreas.

Este projeto contribui para a Segurança da Informação ao permitir:

- Monitoramento de acesso físico
- Identificação de presença em áreas restritas
- Controle de ocupação de ambientes
- Geração de logs de auditoria

Ao detectar automaticamente a presença de pessoas, o sistema funciona como um componente de um sistema de vigilância inteligente, podendo apoiar decisões de segurança, prevenção de acessos indevidos e análise de incidentes.

Assim, o projeto integra Inteligência Artificial e Segurança da Informação para criar uma solução moderna de monitoramento físico.
