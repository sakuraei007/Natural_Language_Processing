# 自然言語処理：言語識別 (Language Identification)

Nグラム言語モデルと各種スムージング手法を用いて、テキストデータの言語を高精度で識別するプログラムです。

## システム構成 (System Structure)

本プロジェクトは、異なるモデリングとスムージング手法を比較・実装した3つの主要ファイルで構成されています。

* **ファイル1: 文字言語識別モデル (Letter Language Identifier)**
  * 文字レベル（Character-level）の頻度に基づく言語識別モデルです。
* **ファイル2: 単語バイグラムモデル (Word Bigram - Laplace & MLE)**
  * 単語レベルのバイグラムモデルです。内部は2つのコードセルに分かれています。
  * **上部のセル:** 未知のバイグラムに対処するための**ラプラス・スムージング (Laplace Smoothing)** を適用。
  * **下部のセル:** スムージングなしの**最尤推定 (MLE: Maximum Likelihood Estimation)** を実行。
* **`wordLangID2.ipynb`: 単語バイグラムモデル (Good-Turing)**
  * **Good-Turingスムージング**を適用した単語バイグラムモデルです。
  * *注記:* 確率がゼロになることによる対数計算のエラーを防ぐため、コードの先頭で微小な定数（`tinyNum = 1e-12`）を定義しています。
 
* ---

* # Natural Language Processing: Language Identification

This project utilizes n-gram language modeling and various smoothing techniques to accurately identify the language of provided text data. 

## System Structure

The repository is organized into three main files, each testing a different modeling or smoothing approach:

* **File 1: Letter Language Identifier**
  * Implements a character-level model to identify languages based on letter frequencies.
* **File 2: Word Bigram Model (Laplace & MLE)**
  * Implements a word-level bigram model. 
  * **Top Cell:** Applies **Laplace smoothing** to account for unseen bigrams.
  * **Bottom Cell:** Calculates the Maximum Likelihood Estimation (**MLE**) without any smoothing techniques.
* **`wordLangID2.ipynb` (Good-Turing)**
  * Implements a word bigram model using **Good-Turing smoothing**.
  * *Note:* A constant (`tinyNum = 1e-12`) is defined at the top of the file to handle zero-probabilities and keep logarithmic calculations clean.
