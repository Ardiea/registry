
---
title: "getWorkerPool"
title_tag: "google-native.cloudbuild/v1alpha2.getWorkerPool"
meta_desc: "Documentation for the google-native.cloudbuild/v1alpha2.getWorkerPool function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Returns details of a `WorkerPool`.




## Using getWorkerPool {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getWorkerPool<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetWorkerPoolArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetWorkerPoolResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_worker_pool(</span><span class="nx">project</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">worker_pool_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetWorkerPoolResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupWorkerPool<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupWorkerPoolArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupWorkerPoolResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupWorkerPool` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetWorkerPool </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetWorkerPoolResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetWorkerPoolArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="workerpoolid_csharp">
<a href="#workerpoolid_csharp" style="color: inherit; text-decoration: inherit;">Worker<wbr>Pool<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_csharp">
<a href="#project_csharp" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="workerpoolid_go">
<a href="#workerpoolid_go" style="color: inherit; text-decoration: inherit;">Worker<wbr>Pool<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_go">
<a href="#project_go" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="workerpoolid_nodejs">
<a href="#workerpoolid_nodejs" style="color: inherit; text-decoration: inherit;">worker<wbr>Pool<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_nodejs">
<a href="#project_nodejs" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="worker_pool_id_python">
<a href="#worker_pool_id_python" style="color: inherit; text-decoration: inherit;">worker_<wbr>pool_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_python">
<a href="#project_python" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## getWorkerPool Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createtime_csharp">
<a href="#createtime_csharp" style="color: inherit; text-decoration: inherit;">Create<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Time at which the request to create the `WorkerPool` was received.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="deletetime_csharp">
<a href="#deletetime_csharp" style="color: inherit; text-decoration: inherit;">Delete<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Time at which the request to delete the `WorkerPool` was received.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource name of the `WorkerPool`. Format of the name is `projects/{project_id}/workerPools/{worker_pool_id}`, where the value of {worker_pool_id} is provided in the CreateWorkerPool request.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="networkconfig_csharp">
<a href="#networkconfig_csharp" style="color: inherit; text-decoration: inherit;">Network<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkconfigresponse">Pulumi.<wbr>Google<wbr>Native.<wbr>Cloud<wbr>Build.<wbr>V1Alpha2.<wbr>Outputs.<wbr>Network<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Network configuration for the `WorkerPool`.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="region_csharp">
<a href="#region_csharp" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Immutable. The region where the `WorkerPool` runs. Only "us-central1" is currently supported. Note that `region` cannot be changed once the `WorkerPool` is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_csharp">
<a href="#state_csharp" style="color: inherit; text-decoration: inherit;">State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}WorkerPool state.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updatetime_csharp">
<a href="#updatetime_csharp" style="color: inherit; text-decoration: inherit;">Update<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Time at which the request to update the `WorkerPool` was received.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="workerconfig_csharp">
<a href="#workerconfig_csharp" style="color: inherit; text-decoration: inherit;">Worker<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#workerconfigresponse">Pulumi.<wbr>Google<wbr>Native.<wbr>Cloud<wbr>Build.<wbr>V1Alpha2.<wbr>Outputs.<wbr>Worker<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Worker configuration for the `WorkerPool`.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createtime_go">
<a href="#createtime_go" style="color: inherit; text-decoration: inherit;">Create<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Time at which the request to create the `WorkerPool` was received.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="deletetime_go">
<a href="#deletetime_go" style="color: inherit; text-decoration: inherit;">Delete<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Time at which the request to delete the `WorkerPool` was received.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource name of the `WorkerPool`. Format of the name is `projects/{project_id}/workerPools/{worker_pool_id}`, where the value of {worker_pool_id} is provided in the CreateWorkerPool request.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="networkconfig_go">
<a href="#networkconfig_go" style="color: inherit; text-decoration: inherit;">Network<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkconfigresponse">Network<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Network configuration for the `WorkerPool`.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="region_go">
<a href="#region_go" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Immutable. The region where the `WorkerPool` runs. Only "us-central1" is currently supported. Note that `region` cannot be changed once the `WorkerPool` is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_go">
<a href="#state_go" style="color: inherit; text-decoration: inherit;">State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}WorkerPool state.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updatetime_go">
<a href="#updatetime_go" style="color: inherit; text-decoration: inherit;">Update<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Time at which the request to update the `WorkerPool` was received.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="workerconfig_go">
<a href="#workerconfig_go" style="color: inherit; text-decoration: inherit;">Worker<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#workerconfigresponse">Worker<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Worker configuration for the `WorkerPool`.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createtime_nodejs">
<a href="#createtime_nodejs" style="color: inherit; text-decoration: inherit;">create<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Time at which the request to create the `WorkerPool` was received.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="deletetime_nodejs">
<a href="#deletetime_nodejs" style="color: inherit; text-decoration: inherit;">delete<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Time at which the request to delete the `WorkerPool` was received.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource name of the `WorkerPool`. Format of the name is `projects/{project_id}/workerPools/{worker_pool_id}`, where the value of {worker_pool_id} is provided in the CreateWorkerPool request.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="networkconfig_nodejs">
<a href="#networkconfig_nodejs" style="color: inherit; text-decoration: inherit;">network<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkconfigresponse">Network<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Network configuration for the `WorkerPool`.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="region_nodejs">
<a href="#region_nodejs" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Immutable. The region where the `WorkerPool` runs. Only "us-central1" is currently supported. Note that `region` cannot be changed once the `WorkerPool` is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_nodejs">
<a href="#state_nodejs" style="color: inherit; text-decoration: inherit;">state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}WorkerPool state.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updatetime_nodejs">
<a href="#updatetime_nodejs" style="color: inherit; text-decoration: inherit;">update<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Time at which the request to update the `WorkerPool` was received.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="workerconfig_nodejs">
<a href="#workerconfig_nodejs" style="color: inherit; text-decoration: inherit;">worker<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#workerconfigresponse">Worker<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Worker configuration for the `WorkerPool`.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="create_time_python">
<a href="#create_time_python" style="color: inherit; text-decoration: inherit;">create_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Time at which the request to create the `WorkerPool` was received.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="delete_time_python">
<a href="#delete_time_python" style="color: inherit; text-decoration: inherit;">delete_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Time at which the request to delete the `WorkerPool` was received.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The resource name of the `WorkerPool`. Format of the name is `projects/{project_id}/workerPools/{worker_pool_id}`, where the value of {worker_pool_id} is provided in the CreateWorkerPool request.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="network_config_python">
<a href="#network_config_python" style="color: inherit; text-decoration: inherit;">network_<wbr>config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkconfigresponse">Network<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Network configuration for the `WorkerPool`.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="region_python">
<a href="#region_python" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Immutable. The region where the `WorkerPool` runs. Only "us-central1" is currently supported. Note that `region` cannot be changed once the `WorkerPool` is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_python">
<a href="#state_python" style="color: inherit; text-decoration: inherit;">state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}WorkerPool state.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="update_time_python">
<a href="#update_time_python" style="color: inherit; text-decoration: inherit;">update_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Time at which the request to update the `WorkerPool` was received.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="worker_config_python">
<a href="#worker_config_python" style="color: inherit; text-decoration: inherit;">worker_<wbr>config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#workerconfigresponse">Worker<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Worker configuration for the `WorkerPool`.{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="networkconfigresponse">Network<wbr>Config<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="peerednetwork_csharp">
<a href="#peerednetwork_csharp" style="color: inherit; text-decoration: inherit;">Peered<wbr>Network</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Immutable. The network definition that the workers are peered to. If this section is left empty, the workers will be peered to WorkerPool.project_id on the default network. Must be in the format `projects/{project}/global/networks/{network}`, where {project} is a project number, such as `12345`, and {network} is the name of a VPC network in the project.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="peerednetwork_go">
<a href="#peerednetwork_go" style="color: inherit; text-decoration: inherit;">Peered<wbr>Network</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Immutable. The network definition that the workers are peered to. If this section is left empty, the workers will be peered to WorkerPool.project_id on the default network. Must be in the format `projects/{project}/global/networks/{network}`, where {project} is a project number, such as `12345`, and {network} is the name of a VPC network in the project.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="peerednetwork_nodejs">
<a href="#peerednetwork_nodejs" style="color: inherit; text-decoration: inherit;">peered<wbr>Network</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Immutable. The network definition that the workers are peered to. If this section is left empty, the workers will be peered to WorkerPool.project_id on the default network. Must be in the format `projects/{project}/global/networks/{network}`, where {project} is a project number, such as `12345`, and {network} is the name of a VPC network in the project.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="peered_network_python">
<a href="#peered_network_python" style="color: inherit; text-decoration: inherit;">peered_<wbr>network</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Immutable. The network definition that the workers are peered to. If this section is left empty, the workers will be peered to WorkerPool.project_id on the default network. Must be in the format `projects/{project}/global/networks/{network}`, where {project} is a project number, such as `12345`, and {network} is the name of a VPC network in the project.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="workerconfigresponse">Worker<wbr>Config<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="disksizegb_csharp">
<a href="#disksizegb_csharp" style="color: inherit; text-decoration: inherit;">Disk<wbr>Size<wbr>Gb</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Size of the disk attached to the worker, in GB. See https://cloud.google.com/compute/docs/disks/ If `0` is specified, Cloud Build will use a standard disk size.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="machinetype_csharp">
<a href="#machinetype_csharp" style="color: inherit; text-decoration: inherit;">Machine<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Machine Type of the worker, such as n1-standard-1. See https://cloud.google.com/compute/docs/machine-types. If left blank, Cloud Build will use a standard unspecified machine to create the worker pool.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="disksizegb_go">
<a href="#disksizegb_go" style="color: inherit; text-decoration: inherit;">Disk<wbr>Size<wbr>Gb</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Size of the disk attached to the worker, in GB. See https://cloud.google.com/compute/docs/disks/ If `0` is specified, Cloud Build will use a standard disk size.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="machinetype_go">
<a href="#machinetype_go" style="color: inherit; text-decoration: inherit;">Machine<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Machine Type of the worker, such as n1-standard-1. See https://cloud.google.com/compute/docs/machine-types. If left blank, Cloud Build will use a standard unspecified machine to create the worker pool.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="disksizegb_nodejs">
<a href="#disksizegb_nodejs" style="color: inherit; text-decoration: inherit;">disk<wbr>Size<wbr>Gb</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Size of the disk attached to the worker, in GB. See https://cloud.google.com/compute/docs/disks/ If `0` is specified, Cloud Build will use a standard disk size.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="machinetype_nodejs">
<a href="#machinetype_nodejs" style="color: inherit; text-decoration: inherit;">machine<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Machine Type of the worker, such as n1-standard-1. See https://cloud.google.com/compute/docs/machine-types. If left blank, Cloud Build will use a standard unspecified machine to create the worker pool.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="disk_size_gb_python">
<a href="#disk_size_gb_python" style="color: inherit; text-decoration: inherit;">disk_<wbr>size_<wbr>gb</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Size of the disk attached to the worker, in GB. See https://cloud.google.com/compute/docs/disks/ If `0` is specified, Cloud Build will use a standard disk size.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="machine_type_python">
<a href="#machine_type_python" style="color: inherit; text-decoration: inherit;">machine_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Machine Type of the worker, such as n1-standard-1. See https://cloud.google.com/compute/docs/machine-types. If left blank, Cloud Build will use a standard unspecified machine to create the worker pool.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-google-native">https://github.com/pulumi/pulumi-google-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
