# プロジェクト名
さとうすずみさんの勉強用

### ディレクトリ構造
課題ごとにroot直下にディレクトリを作っていく。それぞれのディレクトリ内の構造は課題ごとに扱う言語やプロジェクトの規約に従う。

### Githubの使い方フロー
1. (初回のみ)Macなら自分の端末のターミナルで好きな場所に移動し、`git clone git@github.com:ishiwara51/satoStudy.git`を実行する。SSH通信を用いるため公開鍵認証が必要となるので、調べて公開鍵認証の環境を整えておく。以降、ターミナルからの操作はsatoStudy直下で行う。
2. 課題を開始する前に、masterブランチで`git pull`を実行してプロジェクトを最新の状態に更新する。
3. 課題を開始する際、`git branch xxx`を実行してその課題用のブランチを切る。xxxはその課題用のブランチ名を考えて置き換えること。'git checkout xxx'でそのブランチに移動したあと、その課題用のフォルダをsatoStudyの直下に作成（Finderなどで行なって良い）し、コードやプロジェクトをそのフォルダの中に作成していく。
4. 課題が終わったら（小課題がある場合は小課題一つが終わるごとに）'git add -A | git commit'を実行し、変更をローカルリポジトリにコミットする。コミットメッセージの書き方は https://github.com/google/eng-practices のThe Change Author's Guideに準拠する。
5. 課題（小課題全てを含む）が終わって全てコミットしたら、`git push origin xxx`を実行して変更をリモートリポジトリにプッシュする。絶対に`git push origin master`としないこと。
6. ブラウザでhttps://github.com/ishiwara51/satoStudy に移動し、自分がプッシュしたブランチに移動して、変更が正しく反映されていることを確認したらPull Request（以下PR）を作成する。PRのメッセージにはテンプレートが指定してあるので、それに従う。
7. PR上のFileChangedで変更箇所を自分で再度確認してから、加納にレビューを申請する。修正指示が来た場合は4に戻って修正を行う。
8. PRがマージされたらmasterブランチにcheckoutして`git pull`をしてから`git branch -d xxx`でブランチを削除する。課題終わり。