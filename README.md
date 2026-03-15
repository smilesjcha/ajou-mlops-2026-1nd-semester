# AI융합실전프로젝트03 - MLOps

아주대학교 AI대학원\
2026년 1학기

본 저장소는 **AI융합실전프로젝트03 - MLOps** 강의를 위한 실습 코드
저장소입니다.

학생들은 본 Repository를 기반으로 다음 내용을 실습합니다.

-   데이터 분석 (EDA)
-   머신러닝 모델링
-   AutoML 활용
-   MLOps 인프라 (Git / DVC)
-   모델 실험 관리
-   모델 API 배포

최종적으로 **End-to-End Machine Learning Pipeline 구축 경험**을 목표로
합니다.

------------------------------------------------------------------------

# Repository Structure Example

    ajou-mlops-2026-1nd-semester
    │
    ├─ week01_mlops_intro
    ├─ week02_data_ops
    ├─ week03_mlops_infra
    │
    ├─ assignments
    │
    ├─ capstone_project
    │
    ├─ pyproject.toml
    ├─ .env.sample
    └─ README.md

------------------------------------------------------------------------

# Environment Setup

본 강의에서는 **Python 환경 관리 도구로 `uv`를 사용합니다.**

uv는 다음 기능을 통합 제공하는 **최신 Python toolchain**입니다.

-   Python version 관리
-   dependency 관리
-   virtual environment 생성

기존 방식

-   pyenv
-   virtualenv
-   pip

대신 **uv 기반 환경 관리**를 사용합니다.

------------------------------------------------------------------------

# 1. uv 설치

Mac / Linux

``` bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

설치 확인

``` bash
uv --version
```

------------------------------------------------------------------------

# 2. Python 설치

강의에서는 **Python 3.12** 사용을 권장합니다.
2주차 EDA Part에서는 Python 3.8을 필요로 합니다.

``` bash
uv python install 3.12
```

------------------------------------------------------------------------

# 3. Repository Clone

``` bash
git clone https://github.com/smilesjcha/ajou-mlops-2026-1nd-semester.git

cd ajou-mlops-2026-1nd-semester
```

------------------------------------------------------------------------

# 4. Virtual Environment 생성

``` bash
uv venv
```

환경 활성화

Mac / Linux

``` bash
source .venv/bin/activate
```

------------------------------------------------------------------------

# 5. 패키지 설치

강의에서 사용되는 주요 패키지

-   numpy
-   pandas
-   matplotlib
-   seaborn
-   missingno
-   sweetviz
-   ydata-profiling
-   scikit-learn
-   ucimlrepo
-   autogluon

설치 예시

``` bash
uv add numpy pandas matplotlib seaborn
uv add scikit-learn
uv add sweetviz ydata-profiling missingno
uv add ucimlrepo
uv add autogluon
```

또는

``` bash
uv sync
```

------------------------------------------------------------------------

# 6. 환경 변수 설정

``` bash
cp .env.sample .env
```

`.env` 파일을 열어 필요한 값을 입력합니다.

예시

    OPENAI_API_KEY=your_api_key

------------------------------------------------------------------------

# 주요 Python 패키지

  Category         Library
  ---------------- --------------------------------------
  Data Analysis    pandas, numpy
  Visualization    matplotlib, seaborn
  EDA Automation   sweetviz, ydata-profiling, missingno
  ML Framework     scikit-learn
  Dataset Loader   ucimlrepo
  AutoML           autogluon

------------------------------------------------------------------------

# 과제 제출

과제는 다음 방식으로 제출합니다.

1.  개인 GitHub Repository 생성
2.  과제 코드 업로드
3.  Repository 링크 LMS 제출

------------------------------------------------------------------------

# Capstone Project

학기 말에는 **MLOps 기반 End-to-End 프로젝트**를 수행합니다.

프로젝트 예시

-   데이터 수집 및 전처리
-   Feature Engineering
-   ML 모델 학습
-   Experiment Tracking
-   Model API Serving
-   Deployment

------------------------------------------------------------------------

# License

MIT License

본 저장소의 코드는 **교육 및 연구 목적**으로 자유롭게 사용할 수
있습니다.
