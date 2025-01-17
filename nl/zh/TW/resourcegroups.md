---



copyright:

  years: 2017, 2019
lastupdated: "2019-05-21"

keywords: resource group, account resources, users access to resource groups, create resource group

subcollection: resources

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:note: .note}

# 建立及管理資源群組
{: #rgs}

資源群組可讓您用可自訂的分組來組織帳戶資源，以便您可以一次將對多個資源的存取權快速指派給使用者。使用 {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) 存取控制來管理的任何帳戶資源，都屬於您帳戶內的資源群組。Cloud Foundry 服務會指派給組織和空間，而且不能新增至資源群組。

若要開始管理資源群組，請移至**管理** &gt; **帳戶**。展開**帳戶資源**，然後選取**資源群組**。從這裡，您可以檢視資源群組、新增資源、將其重新命名、管理存取權，以及建立新的資源群組。如需使用資源群組的相關資訊，請參閱[用資源群組組織資源的最佳作法](/docs/resources?topic=resources-bp_resourcegroups)。


## 建立資源群組
{: #create_rgs}

如果您具有「隨收隨付制」或「訂閱」帳戶，則可以建立多個資源群組來輕鬆地管理配額，以及檢視一組資源的計費用量。您也可以將資源分組，以便更輕鬆地同時將對多個實例的存取權指派給使用者。請務必注意，您可以重新命名資源群組，但在建立資源群組之後即無法將它刪除。

您必須獲指派具有所有帳戶管理服務之「管理者」角色的 IAM 原則，才能建立更多的資源群組。如果您有「精簡」帳戶或 30 天試用，您無法建立額外的資源群組，但可以將 default 資源群組重新命名。

資源群組與 Cloud Foundry 組織或空間之間的連線受限於您的配額。如需相關資訊，請參閱[何謂別名？](/docs/resources?topic=resources-connect_app#what_is_alias)。
{: note}

1. 移至**管理** &gt; **帳戶**。展開**帳戶資源**，然後選取**資源群組**。
2. 按一下**建立資源群組**。
3. 輸入資源群組的名稱。
4. 按一下**新增**。

## 新增資源至資源群組
{: #add_to_rgs}

使用 IAM 來管理的服務屬於資源群組，而不屬於 Cloud Foundry 組織或空間。當您從型錄建立其中一個服務的服務實例時，系統會提示您將實例指派給資源群組。建立實例時，您所選擇的資源群組便是最終的資源群組，因此無法變更。

對於帳戶中要能從型錄建立資源並將其指派給資源群組的使用者，必須為他們指派兩個存取原則：

* 對資源群組本身具有檢視者角色或更高角色的原則
* 對帳戶中的服務具有編輯者角色或更高角色的原則

## 檢視資源群組內的資源
{: #view_rg_resources}

為了方便檢視資源群組內包含的資源，請從資源清單依資源群組進行過濾。

## 重新命名資源群組
{: #rename_rgs}

您的第一個資源群組會建立並命名為 `Default`。您可以選擇更新此群組或您建立之任何其他群組的名稱。

1. 移至**管理** &gt; **帳戶**。展開**帳戶資源**，然後選取**資源群組**。
2. 從**動作** ![「動作清單」圖示](../icons/action-menu-icon.svg) 功能表中，選取**重新命名**。
3. 輸入唯一名稱，然後按一下**儲存**。

## 使用 {{site.data.keyword.Bluemix_notm}} CLI 管理資源群組及資源
{: #rgs_cli}

{{site.data.keyword.Bluemix_notm}} CLI 具有多個支援資源管理的指令。如需相關資訊，請參閱[使用資源和資源群組](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource#ibmcloud_commands_resource)。

## 管理對資源群組的存取權
{: #rgs_manage_access}

Cloud IAM 可讓您彈性地提供使用者對帳戶中資源的精細存取權。您可以使用 Cloud IAM 將原則指派給使用者，讓使用者可以存取資源群組中的所有資源、資源群組內的單一服務類型，或帳戶中的個別服務實例。為使用者提供對資源群組內之資源的存取權，並不會提供他們管理資源群組本身用的存取權。您可以設定存取權，以個別檢視、編輯及管理實際的資源群組。

如需相關資訊，請參閱[管理對資源的存取權](/docs/iam?topic=iam-iammanidaccser)。
