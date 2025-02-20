You enable semantic search at the service level and, once it is enabled, semantic search is available for all indexes. Semantic search cannot be enabled or disabled on  a per-index basis.

## Enable semantic search

Before enabling semantic search, you must have an Azure Cognitive Search service with at least one index.

> [!NOTE]
> For semantic search, the Cognitive Search service must have a billable tier. You cannot change the pricing tier of a Cognitive Search service. If you need another pricing tier, you will have to re-create the service.

Semantic search is not available in every region. Before enabling semantic search, check that the region of your Cognitive Search service supports semantic search.
To see a list of regions that support semantic search, see [Products available by region](https://azure.microsoft.com/explore/global-infrastructure/products-by-region/?products=search)

To enable semantic search in the Azure portal, perform the following steps:

1. Open the Azure portal and sign in.
1. Select **All resources** and select your search service.
1. In the navigation pane, select **Semantic search (preview)**.
1. Select the appropriate service plan. You can alter the service plan after deployment.

## Configure semantic ranking

Once you have enabled semantic search, you can configure semantic ranking on a per-index basis. You can have multiple semantic configurations on each index.

To configure semantic ranking, follow these steps:

1. From the Azure portal home page, select **All resources** and select your search service.
1. On the navigation bar, in **Search management**, select **Indexes**.

    :::image type="content" source="../media/3-indexes.png" alt-text="Screenshot of Indexes button.":::

1. Select your index.
1. Select **Semantic configurations** and select **Add semantic configuration**.
1. In **Name** type a name for your semantic configuration.
1. In **Title field** select the field that describes the document.
1. Under **Content fields**, in **Field name**, select a content field.
1. Repeat the previous step for additional content fields.
1. Under **Keyword fields**, in **Field name**, select a field with key phrases.
1. Repeat the previous step for additional keyword fields.
1. Select **Save**.
1. On your index page, select **Save**.
