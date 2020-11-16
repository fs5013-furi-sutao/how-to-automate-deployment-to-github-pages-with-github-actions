# GitHub Actions で GitHub Pages へのデプロイを自動化する方法

リポジトリの Actions タブを押し、「set up workflow yourself」リンクをクリックする。

![リポジトリの Actions タブ](./actions-tab-on-repository.png)

workflow ファイルを以下の内容で、「gh-pages.yml」として「Start commit」ボタンをクリックする。

![workflow を記述した yml ファイルをコミット](./gh-pages-yml.png)

これで、`./.github/workflow/` ディレクトリに yml ファイルがコミットされる。

コミットが確認出来たら、`git pull` で workflow ファイルをプルする。

この状態になれば、自動デプロイ環境は整っている。

試しに、ローカルを変更し、コミット、プッシュを行う。main ブランチへのプッシュをトリガに GitHub Actions が起動する。

![GitHub Actions が起動](./deploying-with-github-actions.png)

大きなプロジェクトでなければ、20 ～ 30 秒ほどでデプロイが完了する。

![デプロイ完了](./finish-to-deploy-with-github-actions.png)
