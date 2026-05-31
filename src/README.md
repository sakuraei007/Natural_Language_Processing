# 言語識別プログラム (Language Identifier)

本プログラムは、英語、イタリアン、フランス語のコーパスを使用して学習を行い、入力されたテキストの言語を識別します。Nグラムモデルを用いて言語統計を算出し、識別精度の検証が可能です。

## 使用方法 (How to Use)
1. **学習 (Training):** 学習用のコーパスデータを `Input` フォルダ内の各ファイルに配置してください。
   - `LangID.train.French`
   - `LangID.train.Italian`
   - `LangID.train.English`
2. **検証 (Validation):** - 識別したいテキストを `Validations/LangID.test` ファイルに配置します（各文章を1行ずつ記述してください）。
   - `labels.sol` に正解ラベルを以下の形式で記述します：`[行番号] [言語]` （例: `1 English`）。
3. **実行 (Execution):** `Code` フォルダ内の使用したいNグラムモデルのノートブックを開き、「すべて実行 (Run All)」を選択することで、言語識別を行い、正解データに基づく精度を確認できます。

---
# Language Identifier

# This program will take in 3 files of corpus text (for training), each differing languages from the Input folder, "LangID.train.French", "LangID.train.Italian", and "LangID.train.English", respectively. You should insert a text file to each of these files to allow the model to calculate the statistics it needs in order to predict the languages being used later on. The next step is to go to the "Validations" folder, and to import the text file that you want to test the language classifier on into the file "LangID.test". The format of the text to be imported must be in a format such that each distinct sentence is on a seperate line in the text file. Additionally, it is important that "labels.sol" has the correct answers written within it in the format:

# [line number (starting from 1)] English (if the correct answer for that line is English)


# It will then determine what language is being inputted to the program and output the accuracy compared to the validated solution within the .ipynb code file.

# To run the code, input any three different types of texts into the corresponding English, French, or Italian LangIDtraining file, along with the validated solution in the Validation folder. Then go to the Code folder and choose which n-gram model to use, and click "run all" to see the results.
