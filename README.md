# Parâmetros de Inferência em LLMs: Uma Exploração Estocástica

Este repositório apresenta um estudo detalhado sobre os mecanismos que controlam a geração de texto em Grandes Modelos de Linguagem (LLMs). O projeto explora a transição dos modelos de uma decodificação puramente determinística para amostragens probabilísticas, analisando como a manipulação de **Logits** e **Probabilidades** influencia a criatividade e a coerência das saídas.

## 🚀 Ambiente de Execução

> [!IMPORTANT]
> **Este projeto foi desenvolvido e otimizado para o Google Colab.**
> Devido ao uso intensivo de tensores com PyTorch e à necessidade de aceleração por GPU para a inferência do modelo **Phi-2**, recomenda-se fortemente a execução através do ambiente Colab para garantir a compatibilidade de bibliotecas e recursos de hardware.

## 📚 Conteúdo do Estudo

O notebook está organizado de forma didática, integrando teoria estatística, implementações em Python/PyTorch e visualizações gráficas:

* **Fundamentos**: Conversão de Logits em Probabilidades via função Softmax.
* **Escalonamento de Temperatura ()**: Modulação da entropia da distribuição para controle de criatividade.
* **Amostragem Top-K**: Restrição do espaço amostral aos  tokens mais prováveis.
* **Amostragem Top-P (Nucleus Sampling)**: Filtragem dinâmica baseada na massa de probabilidade acumulada.
* **Demonstração Prática**: Testes de inferência utilizando o modelo **Phi-2** da Microsoft, explorando o impacto real de cada parâmetro na geração de texto.

## 🛠️ Tecnologias Utilizadas

* **Linguagem**: Python 3.12+
* **Framework**: PyTorch (Manipulação de Tensores)
* **Modelos**: Microsoft Phi-2 via Hugging Face Transformers
* **Visualização**: Matplotlib e Pandas

## 📖 Referências

Este trabalho utiliza como base principal o livro **"Build a Large Language Model (From Scratch)"** de Sebastian Raschka e as implementações de referência da biblioteca **Transformers** da Hugging Face. Abaixo estão listadas as referências bibliográficas e tecnológicas que fundamentaram o desenvolvimento deste notebook e a implementação dos parâmetros de inferência:

* **HOLTZMAN, Ari et al.** The Curious Case of Neural Text Degeneration. *In: International Conference on Learning Representations (ICLR)*, 2020. Disponível em: https://arxiv.org/abs/1904.09751. (Referência principal para a técnica de **Amostragem Top-P**).

* **HUGGING FACE.** Transformers Documentation: LogitsProcessor. Disponível em: https://huggingface.co/docs/transformers/main/en/internal/generation_utils. (Base para a implementação das funções de amostragem e uso do modelo **Phi-2**).

* **HUGGING FACE - Phi-2.** Transformers Documentation: **Phi-2**. Disponível em: https://huggingface.co/microsoft/phi-2.

* **MICROSOFT.** Phi-2: The surprising power of small language models. *Microsoft Research Blog*, 2023. Disponível em: https://www.microsoft.com/en-us/research/blog/phi-2-the-surprising-power-of-small-language-models/. (Referência do modelo utilizado na demonstração prática).

* **RASCHKA, Sebastian.** *Build a Large Language Model (From Scratch)*. Shelter Island, NY: Manning Publications, 2024. (Referência para os fundamentos de arquitetura de LLMs e estratégias de decodificação).

* **PYTORCH.**. Disponível em: https://pytorch.org/docs/stable/tensors.html. (Referência técnica para as operações de tensores utilizadas nas máscaras de logits).
