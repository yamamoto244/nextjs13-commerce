[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fvercel%2Fcommerce&project-name=commerce&repo-name=commerce&demo-title=Next.js%20Commerce&demo-url=https%3A%2F%2Fdemo.vercel.store&demo-image=https%3A%2F%2Fbigcommerce-demo-asset-ksvtgfvnd.vercel.app%2Fbigcommerce.png&env=COMPANY_NAME,SHOPIFY_REVALIDATION_SECRET,SHOPIFY_STORE_DOMAIN,SHOPIFY_STOREFRONT_ACCESS_TOKEN,SITE_NAME,TWITTER_CREATOR,TWITTER_SITE)

# Next.js Commerce

Next.js 13とApp Routerに対応したeコマーステンプレートで、次の機能があります。

- Next.js App Router
- Next.jsのメタデータを使用した最適化されたSEO
- React Server Components（RSC）とSuspense
- ミューテーションのためのサーバーアクション
- Edge Runtime
- 新しいフェッチとキャッシュのパラダイム
- 動的OG画像
- Tailwind CSSでのスタイリング
- Shopifyでのチェックアウトと支払い
- システム設定に基づく自動ライト/ダークモード

<h3 id="v1-note"></h3>

> 注意：Next.js Commerce v1をお探しですか？[コード](https://github.com/vercel/commerce/tree/v1)、[デモ](https://commerce-v1.vercel.store)、および[リリースノート](https://github.com/vercel/commerce/releases/tag/v1)をご覧ください。

## プロバイダー

Vercelは、Next.js Commerceのビジョンと戦略で説明されているように、Shopifyバージョンのみを積極的にメンテナンスします。

代替プロバイダーは、`lib/shopify`ファイルを自分自身の実装に置き換えながら、テンプレートの残りの部分をほとんど変更せずに、このリポジトリをフォークできるはずです。

- Shopify（このリポジトリ）
- [BigCommerce](https://github.com/bigcommerce/nextjs-commerce)（[デモ](https://next-commerce-v2.vercel.app/)）
- [Medusa](https://github.com/medusajs/vercel-commerce)（[デモ](https://medusa-nextjs-commerce.vercel.app/)）
- [Saleor](https://github.com/saleor/nextjs-commerce)（[デモ](https://saleor-commerce.vercel.app/)）
- [Shopware](https://github.com/shopwareLabs/vercel-commerce)（[デモ](https://shopware-vercel-commerce-react.vercel.app/)）
- [Swell](https://github.com/swellstores/verswell-commerce)（[デモ](https://verswell-commerce.vercel.app/)）
- [Umbraco](https://github.com/umbraco/Umbraco.VercelCommerce.Demo)（[デモ](https://vercel-commerce-demo.umbraco.com/)）

> 注意：プロバイダーの方々、デモで同様の製品を使用したい場合は、[これらのアセット](https://drive.google.com/file/d/1q_bKerjrwZgHwCw0ovfUMW6He9VtepO_/view?usp=sharing)をダウンロードできます。

## ローカルで実行する

Next.js Commerceを実行するには、[`.env.example`で定義された環境変数](.env.example)を使用する必要があります。これには[Vercel Environment Variables](https://vercel.com/docs/concepts/projects/environment-variables)を使用することをお勧めしますが、`.env`ファイルが必要です。

> 注意：`.env`ファイルをコミットしないでください。そうすると、他の人がShopifyストアを制御できる秘密が漏れてしまいます。

1. Vercel CLIをインストールします：`npm i -g vercel`
2. ローカルインスタンスをVercelとGitHubアカウントにリンクします（`.vercel`ディレクトリが作成されます）：`vercel link`
3. 環境変数をダウンロードします：`vercel env pull`

```bash
pnpm install
pnpm dev
```

アプリはlocalhost:3000で実行されるはずです。

<details>
  <summary>Expand if you work at Vercel and want to run locally and / or contribute</summary>

1. vc linkを実行します。
1. Vercel Solutionsスコープを選択します。
1. 既存のcommerce-shopifyプロジェクトに接続します。
1. 環境変数を取得するには、vc env pullを実行します。
1. すべてが正常に動作していることを確認するには、pmpm devを実行します。
</details>

## Vercel、Next.js Commerce、およびShopifyの統合ガイド

この包括的な統合ガイドを使用して、Vercel上でヘッドレスShopify CMSとしてShopifyを構成し、Next.js CommerceをヘッドレスShopifyストアフロントとして使用できます
