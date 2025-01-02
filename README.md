Classificação de Tumores Cerebrais com CNN

Este projeto implementa um modelo de Rede Neural Convolucional (CNN) para a classificação de tumores cerebrais em imagens. As imagens estão organizadas em duas categorias: glioma (tumor presente) e no_tumor (sem tumor). O objetivo principal foi construir um modelo robusto para auxiliar no diagnóstico médico por meio da análise automatizada de imagens.

Objetivos
Desenvolver um modelo capaz de identificar tumores cerebrais com alta precisão.
Avaliar o desempenho do modelo utilizando métricas como acurácia, perda (loss), e matriz de confusão.
Garantir generalização adequada para evitar overfitting.
Estrutura do Dataset
Total de imagens: 1154
glioma: 826 imagens
no_tumor: 328 imagens
Divisão dos dados:
Treinamento: 70%
Validação: 15%
Teste: 15%

Metodologia
Pré-processamento das imagens:
Todas as imagens foram redimensionadas para 150x150 pixels.
Normalização dos valores de pixel para o intervalo [0, 1].

Construção do modelo:
Arquitetura baseada em camadas convolucionais e pooling, seguidas de camadas densas.
Função de ativação: ReLU nas camadas intermediárias e Softmax na saída.
Otimizador: Adam.
Função de perda: Categorical Crossentropy.
Treinamento:

Número de épocas: 15
Batch size: 32
Callbacks: Early stopping para evitar overfitting.

Avaliação:
Matrizes de confusão para análise detalhada.
Gráficos de perda (loss) e acurácia para monitorar a evolução do modelo.
Resultados
Matriz de confusão no conjunto de teste:
Verdadeiros Positivos: 124
Verdadeiros Negativos: 52
Falsos Positivos: 0
Falsos Negativos: 8
Acurácia geral no teste: 95,14%.
Perda no teste: 0,3549, indicando bom desempenho, mas com possibilidade de refinamento.
Os gráficos de perda e acurácia confirmaram que o modelo não apresentou overfitting significativo e generalizou bem os dados.

Conclusão
O modelo desenvolvido demonstrou alto potencial na classificação de tumores cerebrais, destacando-se pela precisão e robustez. Os resultados indicam que este tipo de abordagem pode ser utilizado em ambientes clínicos para suporte ao diagnóstico médico. Contudo, melhorias futuras podem ser implementadas, como ajuste fino de hiperparâmetros, expansão do conjunto de dados e aplicação de técnicas de aumento de dados (data augmentation).
