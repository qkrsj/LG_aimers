# LG Aimers AI Competition: Model Optimization Hub

본 저장소는 LG Aimers 경진대회 참여를 위해 다양한 모델 경량화 및 양자화(Quantization) 기법을 연구하고 실험하는 공간입니다. 

## Project Overview
- **배경**: 최근 AI 서비스는 클라우드 기반의 대규모 모델을 넘어, On-Device 환경에서도 빠르고 안정적으로 동작하는 경량 모델에 대한 요구가 급격히 증가하고 있습니다.
특히 응답 지연(latency), 메모리 사용량, 운영 비용 등의 제약으로 인해 모델 크기를 줄이면서도 성능을 유지하는 기술이 중요한 과제로 부상하고 있습니다.
EXAONE은 Global Frontier 급의 Large-scale 모델과 함께, 노트북·모바일 등 제한된 환경에서도 활용 가능한 Small-scale 모델 라인업을 보유하고 있습니다.
그러나 단순히 파라미터 수를 줄이는 방식은 메모리와 속도 측면에서는 유리할 수 있으나, 정확도 저하라는 명확한 한계를 동반합니다.
이에 따라, 모델 크기를 효과적으로 축소하면서도 성능 저하를 최소화하고, 실제 추론 환경에서의 효율을 극대화할 수 있는 경량화 기법을 탐구하는 것이 중요해졌습니다. 
이러한 문제의식을 바탕으로, EXAONE 모델을 대상으로 한 실전 중심의 LLM 경량화를 수행하게 됩니다.
- **목표**: 제한된 컴퓨팅 자원에서 대형 모델의 성능을 극대화하기 위한 최적의 양자화 전략 탐색
- **주요 연구 분야**: Post-Training Quantization (PTQ), GPTQ, AWQ, SmoothQuant
- **기술 스택**: Python, PyTorch, Hugging Face `transformers`, `optimum`, `auto-gptq`, `datasets`, `accelerate`

## 📂 Repository Structure
각 디렉토리는 특정 양자화 기법 또는 실험 단계를 포함합니다.


## 🛠 실험 환경 설정
모든 실험은 **Google Colab** 환경을 기준으로 하며, 하드 코딩을 방지하기 위해 환경 변수나 인자값을 사용합니다.

```bash
# 기본 라이브러리 설치
pip install torch transformers optimum auto-gptq
