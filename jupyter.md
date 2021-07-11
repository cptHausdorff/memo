Jupyter Notebook で Julia 1.6.1 を使う方法など

- このファイルの場所 : https://github.com/cptHausdorff/memo/blob/main/jupyter.md

__注意：試行錯誤の結果のメモなので，不要な手順も混ざっている可能性がある．__


# Julia

- Julia 1.6.1 をインストールした． https://julialang.org/downloads/

# Jpyter Notebook

Anaconda をインストールすると Jupyter Notebook も使えるようになる．
Julia の方で IJulia というパッケージをインストールすると Jupyter Notebook で Julia が使えるようになる．

- Anaconda Individual Edition をインストールする．https://www.anaconda.com/products/individual
- Anaconda Prompt (anaconda3) を起動して`conda install -c conda-forge notebook` を入力して実行した．
- Julia 1.6.1 を起動．REPL で ] とすると `(@v1.6) pkg>` が表示される．`(@v1.6) pkg> add IJulia` とした．数分でインストールが終わる．
- これで Jupyter Notebook (anaconda3) において Julia 1.6.1 が使えるようになっているはず

# 既存の notebook の kernel を Julia 1.6.1 にする方法

- Kernel -> Change kernel -> Julia 1.6.1

# Primes.jl の導入

素数関連のパッケージ

- REPLで `julia> import Pkg; Pkg.add("Primes")`  をする．

# jupyter_contrib_nbextensions の導入

Jupyter Notebook で自動で章番号をつけたりしてくれる

- doc: https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/install.html

# Plots.jl の導入

- REPL で `julia> import Pkg; Pkg.add("Plots")` をする．
- 結構時間かかる．
- Your GR installation is incomplete. Rerunning build step for GR package. のエラーが出る場合は julia> Pkg.build("GR") すれば解決した．

# Distances.jl の導入

Mahalanobis 距離が入っている．

- REPL で `julia> import Pkg; Pkg.add("Distances")` をする．
- インストールはすぐ終わる．
- 




# 参考になるかもしれない情報
- https://nbviewer.jupyter.org/github/genkuroki/msfd28/blob/master/msfd28genkuroki.ipynb



