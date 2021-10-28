
---
title: "getASCDataConnector"
title_tag: "azure-native.securityinsights.getASCDataConnector"
meta_desc: "Documentation for the azure-native.securityinsights.getASCDataConnector function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Represents ASC (Azure Security Center) data connector.
API Version: 2020-01-01.




## Using getASCDataConnector {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getASCDataConnector<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetASCDataConnectorArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetASCDataConnectorResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_asc_data_connector(</span><span class="nx">data_connector_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                           <span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                           <span class="nx">workspace_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                           <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetASCDataConnectorResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupASCDataConnector<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupASCDataConnectorArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupASCDataConnectorResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupASCDataConnector` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetASCDataConnector </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetASCDataConnectorResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetASCDataConnectorArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="dataconnectorid_csharp">
<a href="#dataconnectorid_csharp" style="color: inherit; text-decoration: inherit;">Data<wbr>Connector<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Connector ID{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the user's subscription. The name is case insensitive.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspacename_csharp">
<a href="#workspacename_csharp" style="color: inherit; text-decoration: inherit;">Workspace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the workspace.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="dataconnectorid_go">
<a href="#dataconnectorid_go" style="color: inherit; text-decoration: inherit;">Data<wbr>Connector<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Connector ID{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the user's subscription. The name is case insensitive.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspacename_go">
<a href="#workspacename_go" style="color: inherit; text-decoration: inherit;">Workspace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the workspace.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="dataconnectorid_nodejs">
<a href="#dataconnectorid_nodejs" style="color: inherit; text-decoration: inherit;">data<wbr>Connector<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Connector ID{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the user's subscription. The name is case insensitive.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspacename_nodejs">
<a href="#workspacename_nodejs" style="color: inherit; text-decoration: inherit;">workspace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the workspace.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="data_connector_id_python">
<a href="#data_connector_id_python" style="color: inherit; text-decoration: inherit;">data_<wbr>connector_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Connector ID{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the user's subscription. The name is case insensitive.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspace_name_python">
<a href="#workspace_name_python" style="color: inherit; text-decoration: inherit;">workspace_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the workspace.{{% /md %}}</dd></dl>
{{% /choosable %}}




## getASCDataConnector Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="datatypes_csharp">
<a href="#datatypes_csharp" style="color: inherit; text-decoration: inherit;">Data<wbr>Types</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertsdatatypeofdataconnectorresponse">Pulumi.<wbr>Azure<wbr>Native.<wbr>Security<wbr>Insights.<wbr>Outputs.<wbr>Alerts<wbr>Data<wbr>Type<wbr>Of<wbr>Data<wbr>Connector<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}The available data types for the connector.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="etag_csharp">
<a href="#etag_csharp" style="color: inherit; text-decoration: inherit;">Etag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Etag of the azure resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="subscriptionid_csharp">
<a href="#subscriptionid_csharp" style="color: inherit; text-decoration: inherit;">Subscription<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The subscription id to connect to, and get the data from.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="datatypes_go">
<a href="#datatypes_go" style="color: inherit; text-decoration: inherit;">Data<wbr>Types</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertsdatatypeofdataconnectorresponse">Alerts<wbr>Data<wbr>Type<wbr>Of<wbr>Data<wbr>Connector<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}The available data types for the connector.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="etag_go">
<a href="#etag_go" style="color: inherit; text-decoration: inherit;">Etag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Etag of the azure resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="subscriptionid_go">
<a href="#subscriptionid_go" style="color: inherit; text-decoration: inherit;">Subscription<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The subscription id to connect to, and get the data from.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="datatypes_nodejs">
<a href="#datatypes_nodejs" style="color: inherit; text-decoration: inherit;">data<wbr>Types</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertsdatatypeofdataconnectorresponse">Alerts<wbr>Data<wbr>Type<wbr>Of<wbr>Data<wbr>Connector<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}The available data types for the connector.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="etag_nodejs">
<a href="#etag_nodejs" style="color: inherit; text-decoration: inherit;">etag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Etag of the azure resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="subscriptionid_nodejs">
<a href="#subscriptionid_nodejs" style="color: inherit; text-decoration: inherit;">subscription<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The subscription id to connect to, and get the data from.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="data_types_python">
<a href="#data_types_python" style="color: inherit; text-decoration: inherit;">data_<wbr>types</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertsdatatypeofdataconnectorresponse">Alerts<wbr>Data<wbr>Type<wbr>Of<wbr>Data<wbr>Connector<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}The available data types for the connector.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="etag_python">
<a href="#etag_python" style="color: inherit; text-decoration: inherit;">etag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Etag of the azure resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="subscription_id_python">
<a href="#subscription_id_python" style="color: inherit; text-decoration: inherit;">subscription_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The subscription id to connect to, and get the data from.{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="alertsdatatypeofdataconnectorresponse">Alerts<wbr>Data<wbr>Type<wbr>Of<wbr>Data<wbr>Connector<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="alerts_csharp">
<a href="#alerts_csharp" style="color: inherit; text-decoration: inherit;">Alerts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dataconnectordatatypecommonresponse">Pulumi.<wbr>Azure<wbr>Native.<wbr>Security<wbr>Insights.<wbr>Inputs.<wbr>Data<wbr>Connector<wbr>Data<wbr>Type<wbr>Common<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Alerts data type connection.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="alerts_go">
<a href="#alerts_go" style="color: inherit; text-decoration: inherit;">Alerts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dataconnectordatatypecommonresponse">Data<wbr>Connector<wbr>Data<wbr>Type<wbr>Common<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Alerts data type connection.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="alerts_nodejs">
<a href="#alerts_nodejs" style="color: inherit; text-decoration: inherit;">alerts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dataconnectordatatypecommonresponse">Data<wbr>Connector<wbr>Data<wbr>Type<wbr>Common<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Alerts data type connection.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="alerts_python">
<a href="#alerts_python" style="color: inherit; text-decoration: inherit;">alerts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dataconnectordatatypecommonresponse">Data<wbr>Connector<wbr>Data<wbr>Type<wbr>Common<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Alerts data type connection.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="dataconnectordatatypecommonresponse">Data<wbr>Connector<wbr>Data<wbr>Type<wbr>Common<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_csharp">
<a href="#state_csharp" style="color: inherit; text-decoration: inherit;">State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Describe whether this data type connection is enabled or not.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_go">
<a href="#state_go" style="color: inherit; text-decoration: inherit;">State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Describe whether this data type connection is enabled or not.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_nodejs">
<a href="#state_nodejs" style="color: inherit; text-decoration: inherit;">state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Describe whether this data type connection is enabled or not.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_python">
<a href="#state_python" style="color: inherit; text-decoration: inherit;">state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Describe whether this data type connection is enabled or not.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
