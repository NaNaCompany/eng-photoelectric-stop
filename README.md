# 광전효과 정지전압 계산기

단일 광자 광전효과에서 가장 빠른 광전자를 멈추는 역전압의 크기를 계산한다.

- ID: E116
- App: https://nanalab.kr/eng-photoelectric-stop/
- Repository: https://github.com/NaNaCompany/eng-photoelectric-stop
- Formula: V_stop = (hc/λ − φ)/e, when hc/λ ≥ φ

## Model and data

λ>0이며 φ≥0이다. φ는 사용자가 입력한 해당 표면의 일함수다. 단색광·단일 광자 모델이며 다광자·열전자·접촉전위·표면 오염 효과는 제외한다. hc/λ<φ이면 방출 불가를 표시하고 경계에서는 V_stop=0이다. 결과는 역전압의 부호가 아닌 크기이며 광전류나 양자효율을 예측하지 않는다.

Inputs normalize to SI. Repeated-input models support adding/removing actual input rows. Calculations, finite-number checks and physical-domain checks run locally; no external property database or solver API is used.

## Validation

Run node --test tests/*.test.mjs and python scripts/build-locales.py --check. tests/reference.json contains independently computed high-precision default and boundary references. The source notices distinguish original MIT work from citation-only external references.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
