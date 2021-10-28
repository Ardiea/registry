
---
title: "getJobTargetGroup"
title_tag: "azure-native.sql.getJobTargetGroup"
meta_desc: "Documentation for the azure-native.sql.getJobTargetGroup function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

A group of job targets.
API Version: 2020-11-01-preview.




## Using getJobTargetGroup {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getJobTargetGroup<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetJobTargetGroupArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetJobTargetGroupResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_job_target_group(</span><span class="nx">job_agent_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">server_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">target_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetJobTargetGroupResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupJobTargetGroup<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupJobTargetGroupArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupJobTargetGroupResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupJobTargetGroup` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetJobTargetGroup </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetJobTargetGroupResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetJobTargetGroupArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="jobagentname_csharp">
<a href="#jobagentname_csharp" style="color: inherit; text-decoration: inherit;">Job<wbr>Agent<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the job agent.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="servername_csharp">
<a href="#servername_csharp" style="color: inherit; text-decoration: inherit;">Server<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the server.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="targetgroupname_csharp">
<a href="#targetgroupname_csharp" style="color: inherit; text-decoration: inherit;">Target<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the target group.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="jobagentname_go">
<a href="#jobagentname_go" style="color: inherit; text-decoration: inherit;">Job<wbr>Agent<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the job agent.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="servername_go">
<a href="#servername_go" style="color: inherit; text-decoration: inherit;">Server<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the server.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="targetgroupname_go">
<a href="#targetgroupname_go" style="color: inherit; text-decoration: inherit;">Target<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the target group.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="jobagentname_nodejs">
<a href="#jobagentname_nodejs" style="color: inherit; text-decoration: inherit;">job<wbr>Agent<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the job agent.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="servername_nodejs">
<a href="#servername_nodejs" style="color: inherit; text-decoration: inherit;">server<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the server.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="targetgroupname_nodejs">
<a href="#targetgroupname_nodejs" style="color: inherit; text-decoration: inherit;">target<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the target group.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="job_agent_name_python">
<a href="#job_agent_name_python" style="color: inherit; text-decoration: inherit;">job_<wbr>agent_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the job agent.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group that contains the resource. You can obtain this value from the Azure Resource Manager API or the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="server_name_python">
<a href="#server_name_python" style="color: inherit; text-decoration: inherit;">server_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the server.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="target_group_name_python">
<a href="#target_group_name_python" style="color: inherit; text-decoration: inherit;">target_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the target group.{{% /md %}}</dd></dl>
{{% /choosable %}}




## getJobTargetGroup Result {#result}

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
    <dd>{{% md %}}Resource ID.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="members_csharp">
<a href="#members_csharp" style="color: inherit; text-decoration: inherit;">Members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#jobtargetresponse">List&lt;Pulumi.<wbr>Azure<wbr>Native.<wbr>Sql.<wbr>Outputs.<wbr>Job<wbr>Target<wbr>Response&gt;</a></span>
    </dt>
    <dd>{{% md %}}Members of the target group.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Resource ID.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="members_go">
<a href="#members_go" style="color: inherit; text-decoration: inherit;">Members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#jobtargetresponse">[]Job<wbr>Target<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Members of the target group.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Resource ID.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="members_nodejs">
<a href="#members_nodejs" style="color: inherit; text-decoration: inherit;">members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#jobtargetresponse">Job<wbr>Target<wbr>Response[]</a></span>
    </dt>
    <dd>{{% md %}}Members of the target group.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Resource ID.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="members_python">
<a href="#members_python" style="color: inherit; text-decoration: inherit;">members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#jobtargetresponse">Sequence[Job<wbr>Target<wbr>Response]</a></span>
    </dt>
    <dd>{{% md %}}Members of the target group.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource name.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource type.{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="jobtargetresponse">Job<wbr>Target<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target type.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="databasename_csharp">
<a href="#databasename_csharp" style="color: inherit; text-decoration: inherit;">Database<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target database name.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="elasticpoolname_csharp">
<a href="#elasticpoolname_csharp" style="color: inherit; text-decoration: inherit;">Elastic<wbr>Pool<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target elastic pool name.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="membershiptype_csharp">
<a href="#membershiptype_csharp" style="color: inherit; text-decoration: inherit;">Membership<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Whether the target is included or excluded from the group.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="refreshcredential_csharp">
<a href="#refreshcredential_csharp" style="color: inherit; text-decoration: inherit;">Refresh<wbr>Credential</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID of the credential that is used during job execution to connect to the target and determine the list of databases inside the target.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="servername_csharp">
<a href="#servername_csharp" style="color: inherit; text-decoration: inherit;">Server<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target server name.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="shardmapname_csharp">
<a href="#shardmapname_csharp" style="color: inherit; text-decoration: inherit;">Shard<wbr>Map<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target shard map.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target type.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="databasename_go">
<a href="#databasename_go" style="color: inherit; text-decoration: inherit;">Database<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target database name.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="elasticpoolname_go">
<a href="#elasticpoolname_go" style="color: inherit; text-decoration: inherit;">Elastic<wbr>Pool<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target elastic pool name.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="membershiptype_go">
<a href="#membershiptype_go" style="color: inherit; text-decoration: inherit;">Membership<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Whether the target is included or excluded from the group.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="refreshcredential_go">
<a href="#refreshcredential_go" style="color: inherit; text-decoration: inherit;">Refresh<wbr>Credential</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID of the credential that is used during job execution to connect to the target and determine the list of databases inside the target.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="servername_go">
<a href="#servername_go" style="color: inherit; text-decoration: inherit;">Server<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target server name.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="shardmapname_go">
<a href="#shardmapname_go" style="color: inherit; text-decoration: inherit;">Shard<wbr>Map<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target shard map.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target type.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="databasename_nodejs">
<a href="#databasename_nodejs" style="color: inherit; text-decoration: inherit;">database<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target database name.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="elasticpoolname_nodejs">
<a href="#elasticpoolname_nodejs" style="color: inherit; text-decoration: inherit;">elastic<wbr>Pool<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target elastic pool name.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="membershiptype_nodejs">
<a href="#membershiptype_nodejs" style="color: inherit; text-decoration: inherit;">membership<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Whether the target is included or excluded from the group.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="refreshcredential_nodejs">
<a href="#refreshcredential_nodejs" style="color: inherit; text-decoration: inherit;">refresh<wbr>Credential</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID of the credential that is used during job execution to connect to the target and determine the list of databases inside the target.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="servername_nodejs">
<a href="#servername_nodejs" style="color: inherit; text-decoration: inherit;">server<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target server name.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="shardmapname_nodejs">
<a href="#shardmapname_nodejs" style="color: inherit; text-decoration: inherit;">shard<wbr>Map<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The target shard map.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The target type.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="database_name_python">
<a href="#database_name_python" style="color: inherit; text-decoration: inherit;">database_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The target database name.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="elastic_pool_name_python">
<a href="#elastic_pool_name_python" style="color: inherit; text-decoration: inherit;">elastic_<wbr>pool_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The target elastic pool name.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="membership_type_python">
<a href="#membership_type_python" style="color: inherit; text-decoration: inherit;">membership_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Whether the target is included or excluded from the group.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="refresh_credential_python">
<a href="#refresh_credential_python" style="color: inherit; text-decoration: inherit;">refresh_<wbr>credential</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The resource ID of the credential that is used during job execution to connect to the target and determine the list of databases inside the target.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="server_name_python">
<a href="#server_name_python" style="color: inherit; text-decoration: inherit;">server_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The target server name.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="shard_map_name_python">
<a href="#shard_map_name_python" style="color: inherit; text-decoration: inherit;">shard_<wbr>map_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The target shard map.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
