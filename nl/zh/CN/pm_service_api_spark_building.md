---

copyright:
  years: 2016, 2017
lastupdated: "2017-06-23"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# 构建预测性分析应用程序


本部分描述部署和使用样本应用程序的过程。

**场景名称**：产品系列预测。

**场景描述**：客户在欧洲运营着最著名的连锁店之一。
他们希望我们弄清楚顾客对其产品系列（例如，“个人辅助用具”、“露营装备”和“户外防护用品”）的兴趣。为此，数据研究员开发了一个预测模型并将其与您（开发者）共享。您的任务是准备和部署 Node.js 应用程序，此应用程序通过对已部署的模型发出评分请求来推荐体育用品系列。

1. 登录到 Bluemix，并创建 Machine Learning 的实例。

2. 启动 Machine Learning“仪表板”。

3. 转至“样本”选项卡。

4. 在“样本模型”部分中，找到“产品系列预测”磁贴，并单击“添加模型”按钮 (+)。现在，您将在“模型”选项卡上的可用模型列表中看到样本“产品系列预测”模型。

   **注**：如果要使用自己的 Data Science Experience 项目和模型，而不使用样本，您必须在 Machine Learning 存储库中永久存储定制模型。可以使用 REST API 或客户库来完成此操作。有关详细信息，请参阅“开发和持久存储定制模型”。

5. 在“操作”菜单中，选择“创建部署”以将“产品系列预测”模型部署为联机部署。

6. 指定部署名称（例如，产品系列预测），然后单击“保存”。现在，应该会在“部署”列表中看到“产品系列预测”部署。

7. 在“操作”菜单中，针对部署选择“查看详细信息”。详细信息窗格中显示的“评分端点”将用于运行评分请求。

8. 要通过 REST API 运行评分请求，评分端点和授权令牌是必需的。有关更多信息，请参阅“部署联机模型”。

9. 现在，可以试用以下地址提供的样本 Node.js 应用程序：
   https://github.com/pmservice/product-line-prediction.

   要将样本应用程序代码自动部署到 Bluemix 空间，请转至“样本”选项卡，并在“样本应用程序”部分中，通过单击 (+) 按钮选择“产品系列预测”应用程序以进行部署。在 DeployToBluemix 表单上进行认证（如果提示）。

   现在，应该会在 Bluemix 仪表板的“所有应用程序”部分中看到样本应用程序。

10. 单击应用程序以查看其详细信息。在此，可以修改应用程序详细信息，例如实例数、内存等。

11. 现在，可以将应用程序与 Machine Learning 实例绑定。在“连接”选项卡上，单击“连接现有服务”。重新编译打包后，应用程序会连接到该服务实例。

12. 使用路径地址运行应用程序。

13. 在应用程序中，选择“产品系列预测”部署。现在，您可随时使用样本记录和预测结果。