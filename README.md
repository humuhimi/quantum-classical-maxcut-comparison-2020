# 量子コンピューター2020 / Quantum Computer 2020
MaxCut問題の古典・量子アルゴリズム比較 / Classical-Quantum Algorithm Comparison for MaxCut Problem

## 日本語

### 概要
このリポジトリは、MaxCut問題を解くための古典的手法と量子コンピューティング手法の実装と比較を含んでいます。

本プロジェクトは以下のYouTube動画の解説資料として使用されています：
- [量子コンピューターと古典コンピュータの比較解説動画](https://www.youtube.com/watch?v=9KhLBOW0Pz0&t=9943s)

### 内容

#### MaxCut問題とは
MaxCut問題は、グラフの頂点を2つの集合に分割し、その集合間を結ぶエッジの重みの合計を最大化する組み合わせ最適化問題です。

#### 実装手法

##### 古典的手法
- **SDP（半正定値計画）緩和法**: `maxcut3古典手法.ipynb`
  - PICOS/CVXOPTを使用したSDP緩和による近似解法
  - Goemans-Williamsonアルゴリズムの実装
  - 20ノードおよび100ノードのグラフでの実験

##### 量子コンピューティング手法
- **D-Wave量子アニーリング**: 実装・実験中
  - D-Wave Systems社の量子アニーラーを使用した実験
  - QUBOフォーミュレーションによるMaxCut問題の解法
  - 実機での実行結果と古典手法との比較
- **QAOA（Quantum Approximate Optimization Algorithm）**: 実装予定
- **VQE（Variational Quantum Eigensolver）**: 実装予定

### 必要なライブラリ
```bash
# 古典手法用
pip install cvxopt picos networkx numpy matplotlib

# D-Wave用（オプション）
pip install dwave-ocean-sdk
```

### 使用方法
Jupyter Notebookを起動して、各`.ipynb`ファイルを実行してください：
```bash
jupyter notebook
```

### ファイル構成
- `maxcut3古典手法.ipynb` - SDP緩和を用いた古典的アプローチ
- 他の量子アルゴリズム実装ファイル（追加予定）

### 参考資料
- [動画での解説](https://www.youtube.com/watch?v=9KhLBOW0Pz0&t=9943s) - 本プロジェクトのアルゴリズムの詳細な比較と解説

---

## English

### Overview
This repository contains implementations and comparisons of classical and quantum computing approaches for solving the MaxCut problem.

This project serves as the source material for the following YouTube video:
- [Comparison of Quantum and Classical Computers](https://www.youtube.com/watch?v=9KhLBOW0Pz0&t=9943s)

### Contents

#### What is the MaxCut Problem?
The MaxCut problem is a combinatorial optimization problem where the goal is to partition the vertices of a graph into two sets such that the sum of weights of edges between the two sets is maximized.

#### Implementation Methods

##### Classical Approach
- **SDP (Semidefinite Programming) Relaxation**: `maxcut3古典手法.ipynb`
  - Approximate solution using SDP relaxation with PICOS/CVXOPT
  - Implementation of the Goemans-Williamson algorithm
  - Experiments on graphs with 20 and 100 nodes

##### Quantum Computing Approaches
- **D-Wave Quantum Annealing**: Under implementation and experimentation
  - Experiments using D-Wave Systems' quantum annealer
  - MaxCut problem solving through QUBO formulation
  - Comparison of real quantum hardware results with classical methods
- **QAOA (Quantum Approximate Optimization Algorithm)**: To be implemented
- **VQE (Variational Quantum Eigensolver)**: To be implemented

### Requirements
```bash
# For classical methods
pip install cvxopt picos networkx numpy matplotlib

# For D-Wave (optional)
pip install dwave-ocean-sdk
```

### Usage
Launch Jupyter Notebook and run the `.ipynb` files:
```bash
jupyter notebook
```

### File Structure
- `maxcut3古典手法.ipynb` - Classical approach using SDP relaxation
- Other quantum algorithm implementation files (to be added)

### References
- [Video Explanation](https://www.youtube.com/watch?v=9KhLBOW0Pz0&t=9943s) - Detailed comparison and explanation of the algorithms in this project

---

## ライセンス / License
このプロジェクトはMITライセンスの下で公開されています。
This project is licensed under the MIT License.