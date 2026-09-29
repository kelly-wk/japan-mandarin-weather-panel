# 日本の市町村別ミカン収量と気象のパネル分析 / Municipal Mandarin-Orange Yield–Weather Panel Analysis in Japan

[紹介ページを開く / Open the presentation page](https://kelly-wk.github.io/japan-mandarin-weather-panel/)

> **評価設計修復済み・数値結果非公開 / Evaluation design repaired · numeric results withheld**  
> 公開ケーススタディ / Public case study

## 概要 / Overview

市町村の反復観測を保った分割と将来予測を用い、収量と気象の関連を監査したパネル分析。

An audited yield-weather panel analysis using municipality-preserving splits and explicit forward prediction.

## 主なポイント / Highlights

1. **市町村を分割単位として保持し、同一地域の情報漏洩を防止。**  
   Kept municipalities intact as the splitting unit to prevent same-area leakage.
2. **ランダムホールドアウトと将来時点への外挿を別の検証課題として評価。**  
   Evaluated random holdout and forward extrapolation as distinct validation tasks.
3. **気温との関連が仕様に敏感であることを保持し、因果効果として報告しない。**  
   Retained specification sensitivity in the temperature association and avoided a causal interpretation.

## 研究の流れ / Research Flow

| 段階 / Stage | 内容 / Evidence |
|---|---|
| **課題 / Problem** | 市町村別収量と気象の関係を、地域内相関と時間外挿を考慮して評価する。<br>Assess municipal yield-weather relationships while accounting for within-area dependence and temporal extrapolation. |
| **方法 / Method** | GAMと相関構造付き混合モデルを構築し、訓練フォールド内で共線性を処理する。<br>Fit GAM and correlation-aware mixed models, handling collinearity within training folds. |
| **検証 / Validation** | 市町村グループ交差検証と将来年ホールドアウトを分離して実施する。<br>Run municipality-grouped cross-validation separately from future-year holdout. |
| **成果 / Outcome** | 評価設計を修復し、気象との関連がモデル仕様に依存することを明示した。<br>Repaired the evaluation design and made the model dependence of weather associations explicit. |

## 使用手法 / Methods

R, Generalized additive models, Mixed-effects models, CAR(1) correlation, Municipality-grouped cross-validation, Forward validation, Train-fold orthogonalization

## 限界と適用範囲 / Limitations & Scope

- 授業由来パネルの公開権限、収量単位、上流データの来歴が不明確で、数値結果を公開できない。  
  Publication rights, yield units, and upstream provenance for the course panel are unclear, so numeric results cannot be released.

## 公開範囲 / Publication Boundary

公開ページは評価設計と監査上の学びのみ。データ権利と来歴が未確認のため、実数値、図、市町村情報、派生結果、コードは公開しない。

The public page is limited to evaluation design and audit lessons. Numeric results, figures, municipality details, derived results, and code remain private because data rights and provenance are unresolved.

---

この文書は公開可能な範囲だけで構成されています。  
This document contains only material cleared for public presentation.
