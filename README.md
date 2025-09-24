# ETF Rebalancing Portfolio (Static, Dynamic & ML)

[![Open in Colab – Static](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/<jweon96>/<etf-rebalancing-portfolio>/blob/main/notebooks/static_rebalancing.ipynb)
[![Open in Colab – Dynamic/ML](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/<jweon96>/<etf-rebalancing-portfolio>/blob/main/notebooks/dynamic_rebalancing.ipynb)
![python](https://img.shields.io/badge/python-3.10%2B-blue)
![license](https://img.shields.io/badge/license-MIT-informational)

**SPY/TLT/GLD** 포트폴리오에 대해 **정적(연 1회/밴드)**, **동적(변동성 기반)**, **ML 트리거 기반** 리밸런싱을 구현하고  
**거래비용**을 반영해 성과(CAGR / Sharpe / MaxDD / Vol)를 비교합니다.

## Highlights
- 📊 **Static**: 연 1회, 밴드(±5%, ±10%) 리밸런싱 + 거래비용
- ⚙️ **Dynamic**: 30일 변동성 기반 **동적 밴드**
- 🤖 **ML Trigger**: RF/Logit → 임계값(F1) → 신호=1일에만 리밸런싱
- 💸 비용: `turnover × cost_rate × 포트가치`로 **일별 차감**
- 🧪 비교: 공통 기간 정렬, 상대성과(액티브), 롤링 IR

## Notebooks
- `notebooks/static_rebalancing.ipynb` — 정적 리밸런싱(연1회/밴드) + 비용  
- `notebooks/dynamic_rebalancing.ipynb` — 동적 밴드 + ML 트리거 + 비교 & 진단

## Quick Start
**Colab**: 위 배지 클릭 → 상단 CONFIG(기간/비중/수수료) 조정 → 전체 실행  
**Local**
```bash
git clone https://github.com/<jweon96>/<etf-rebalancing-portfolio>.git
cd <REPO_NAME>
pip install -r requirements.txt
jupyter lab
