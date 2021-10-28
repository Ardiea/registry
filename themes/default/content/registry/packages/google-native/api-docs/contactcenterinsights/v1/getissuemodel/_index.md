
---
title: "getIssueModel"
title_tag: "google-native.contactcenterinsights/v1.getIssueModel"
meta_desc: "Documentation for the google-native.contactcenterinsights/v1.getIssueModel function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Gets an issue model.




## Using getIssueModel {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getIssueModel<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetIssueModelArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetIssueModelResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_issue_model(</span><span class="nx">issue_model_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">location</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">project</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetIssueModelResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupIssueModel<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupIssueModelArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupIssueModelResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupIssueModel` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetIssueModel </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetIssueModelResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetIssueModelArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="issuemodelid_csharp">
<a href="#issuemodelid_csharp" style="color: inherit; text-decoration: inherit;">Issue<wbr>Model<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="location_csharp">
<a href="#location_csharp" style="color: inherit; text-decoration: inherit;">Location</a>
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
        <span id="issuemodelid_go">
<a href="#issuemodelid_go" style="color: inherit; text-decoration: inherit;">Issue<wbr>Model<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="location_go">
<a href="#location_go" style="color: inherit; text-decoration: inherit;">Location</a>
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
        <span id="issuemodelid_nodejs">
<a href="#issuemodelid_nodejs" style="color: inherit; text-decoration: inherit;">issue<wbr>Model<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="location_nodejs">
<a href="#location_nodejs" style="color: inherit; text-decoration: inherit;">location</a>
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
        <span id="issue_model_id_python">
<a href="#issue_model_id_python" style="color: inherit; text-decoration: inherit;">issue_<wbr>model_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="location_python">
<a href="#location_python" style="color: inherit; text-decoration: inherit;">location</a>
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




## getIssueModel Result {#result}

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
    <dd>{{% md %}}The time at which this issue model was created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="displayname_csharp">
<a href="#displayname_csharp" style="color: inherit; text-decoration: inherit;">Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The representative name for the issue model.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="inputdataconfig_csharp">
<a href="#inputdataconfig_csharp" style="color: inherit; text-decoration: inherit;">Input<wbr>Data<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googlecloudcontactcenterinsightsv1issuemodelinputdataconfigresponse">Pulumi.<wbr>Google<wbr>Native.<wbr>Contactcenterinsights.<wbr>V1.<wbr>Outputs.<wbr>Google<wbr>Cloud<wbr>Contactcenterinsights<wbr>V1Issue<wbr>Model<wbr>Input<wbr>Data<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Configs for the input data that used to create the issue model.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Immutable. The resource name of the issue model. Format: projects/{project}/locations/{location}/issueModels/{issue_model}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_csharp">
<a href="#state_csharp" style="color: inherit; text-decoration: inherit;">State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}State of the model.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="trainingstats_csharp">
<a href="#trainingstats_csharp" style="color: inherit; text-decoration: inherit;">Training<wbr>Stats</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googlecloudcontactcenterinsightsv1issuemodellabelstatsresponse">Pulumi.<wbr>Google<wbr>Native.<wbr>Contactcenterinsights.<wbr>V1.<wbr>Outputs.<wbr>Google<wbr>Cloud<wbr>Contactcenterinsights<wbr>V1Issue<wbr>Model<wbr>Label<wbr>Stats<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Immutable. The issue model's label statistics on its training data.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updatetime_csharp">
<a href="#updatetime_csharp" style="color: inherit; text-decoration: inherit;">Update<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The most recent time at which the issue model was updated.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The time at which this issue model was created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="displayname_go">
<a href="#displayname_go" style="color: inherit; text-decoration: inherit;">Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The representative name for the issue model.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="inputdataconfig_go">
<a href="#inputdataconfig_go" style="color: inherit; text-decoration: inherit;">Input<wbr>Data<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googlecloudcontactcenterinsightsv1issuemodelinputdataconfigresponse">Google<wbr>Cloud<wbr>Contactcenterinsights<wbr>V1Issue<wbr>Model<wbr>Input<wbr>Data<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Configs for the input data that used to create the issue model.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Immutable. The resource name of the issue model. Format: projects/{project}/locations/{location}/issueModels/{issue_model}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_go">
<a href="#state_go" style="color: inherit; text-decoration: inherit;">State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}State of the model.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="trainingstats_go">
<a href="#trainingstats_go" style="color: inherit; text-decoration: inherit;">Training<wbr>Stats</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googlecloudcontactcenterinsightsv1issuemodellabelstatsresponse">Google<wbr>Cloud<wbr>Contactcenterinsights<wbr>V1Issue<wbr>Model<wbr>Label<wbr>Stats<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Immutable. The issue model's label statistics on its training data.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updatetime_go">
<a href="#updatetime_go" style="color: inherit; text-decoration: inherit;">Update<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The most recent time at which the issue model was updated.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The time at which this issue model was created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="displayname_nodejs">
<a href="#displayname_nodejs" style="color: inherit; text-decoration: inherit;">display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The representative name for the issue model.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="inputdataconfig_nodejs">
<a href="#inputdataconfig_nodejs" style="color: inherit; text-decoration: inherit;">input<wbr>Data<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googlecloudcontactcenterinsightsv1issuemodelinputdataconfigresponse">Google<wbr>Cloud<wbr>Contactcenterinsights<wbr>V1Issue<wbr>Model<wbr>Input<wbr>Data<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Configs for the input data that used to create the issue model.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Immutable. The resource name of the issue model. Format: projects/{project}/locations/{location}/issueModels/{issue_model}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_nodejs">
<a href="#state_nodejs" style="color: inherit; text-decoration: inherit;">state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}State of the model.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="trainingstats_nodejs">
<a href="#trainingstats_nodejs" style="color: inherit; text-decoration: inherit;">training<wbr>Stats</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googlecloudcontactcenterinsightsv1issuemodellabelstatsresponse">Google<wbr>Cloud<wbr>Contactcenterinsights<wbr>V1Issue<wbr>Model<wbr>Label<wbr>Stats<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Immutable. The issue model's label statistics on its training data.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updatetime_nodejs">
<a href="#updatetime_nodejs" style="color: inherit; text-decoration: inherit;">update<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The most recent time at which the issue model was updated.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The time at which this issue model was created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="display_name_python">
<a href="#display_name_python" style="color: inherit; text-decoration: inherit;">display_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The representative name for the issue model.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="input_data_config_python">
<a href="#input_data_config_python" style="color: inherit; text-decoration: inherit;">input_<wbr>data_<wbr>config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googlecloudcontactcenterinsightsv1issuemodelinputdataconfigresponse">Google<wbr>Cloud<wbr>Contactcenterinsights<wbr>V1Issue<wbr>Model<wbr>Input<wbr>Data<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Configs for the input data that used to create the issue model.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Immutable. The resource name of the issue model. Format: projects/{project}/locations/{location}/issueModels/{issue_model}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_python">
<a href="#state_python" style="color: inherit; text-decoration: inherit;">state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}State of the model.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="training_stats_python">
<a href="#training_stats_python" style="color: inherit; text-decoration: inherit;">training_<wbr>stats</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googlecloudcontactcenterinsightsv1issuemodellabelstatsresponse">Google<wbr>Cloud<wbr>Contactcenterinsights<wbr>V1Issue<wbr>Model<wbr>Label<wbr>Stats<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Immutable. The issue model's label statistics on its training data.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="update_time_python">
<a href="#update_time_python" style="color: inherit; text-decoration: inherit;">update_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The most recent time at which the issue model was updated.{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="googlecloudcontactcenterinsightsv1issuemodelinputdataconfigresponse">Google<wbr>Cloud<wbr>Contactcenterinsights<wbr>V1Issue<wbr>Model<wbr>Input<wbr>Data<wbr>Config<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="filter_csharp">
<a href="#filter_csharp" style="color: inherit; text-decoration: inherit;">Filter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A filter to reduce the conversations used for training the model to a specific subset.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="medium_csharp">
<a href="#medium_csharp" style="color: inherit; text-decoration: inherit;">Medium</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Medium of conversations used in training data. This field is being deprecated. To specify the medium to be used in training a new issue model, set the `medium` field on `filter`.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="trainingconversationscount_csharp">
<a href="#trainingconversationscount_csharp" style="color: inherit; text-decoration: inherit;">Training<wbr>Conversations<wbr>Count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Number of conversations used in training. Output only.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="filter_go">
<a href="#filter_go" style="color: inherit; text-decoration: inherit;">Filter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A filter to reduce the conversations used for training the model to a specific subset.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="medium_go">
<a href="#medium_go" style="color: inherit; text-decoration: inherit;">Medium</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Medium of conversations used in training data. This field is being deprecated. To specify the medium to be used in training a new issue model, set the `medium` field on `filter`.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="trainingconversationscount_go">
<a href="#trainingconversationscount_go" style="color: inherit; text-decoration: inherit;">Training<wbr>Conversations<wbr>Count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Number of conversations used in training. Output only.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="filter_nodejs">
<a href="#filter_nodejs" style="color: inherit; text-decoration: inherit;">filter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A filter to reduce the conversations used for training the model to a specific subset.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="medium_nodejs">
<a href="#medium_nodejs" style="color: inherit; text-decoration: inherit;">medium</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Medium of conversations used in training data. This field is being deprecated. To specify the medium to be used in training a new issue model, set the `medium` field on `filter`.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="trainingconversationscount_nodejs">
<a href="#trainingconversationscount_nodejs" style="color: inherit; text-decoration: inherit;">training<wbr>Conversations<wbr>Count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Number of conversations used in training. Output only.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="filter_python">
<a href="#filter_python" style="color: inherit; text-decoration: inherit;">filter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A filter to reduce the conversations used for training the model to a specific subset.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="medium_python">
<a href="#medium_python" style="color: inherit; text-decoration: inherit;">medium</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Medium of conversations used in training data. This field is being deprecated. To specify the medium to be used in training a new issue model, set the `medium` field on `filter`.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="training_conversations_count_python">
<a href="#training_conversations_count_python" style="color: inherit; text-decoration: inherit;">training_<wbr>conversations_<wbr>count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Number of conversations used in training. Output only.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="googlecloudcontactcenterinsightsv1issuemodellabelstatsresponse">Google<wbr>Cloud<wbr>Contactcenterinsights<wbr>V1Issue<wbr>Model<wbr>Label<wbr>Stats<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="analyzedconversationscount_csharp">
<a href="#analyzedconversationscount_csharp" style="color: inherit; text-decoration: inherit;">Analyzed<wbr>Conversations<wbr>Count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Number of conversations the issue model has analyzed at this point in time.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="issuestats_csharp">
<a href="#issuestats_csharp" style="color: inherit; text-decoration: inherit;">Issue<wbr>Stats</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}Statistics on each issue. Key is the issue's resource name.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="unclassifiedconversationscount_csharp">
<a href="#unclassifiedconversationscount_csharp" style="color: inherit; text-decoration: inherit;">Unclassified<wbr>Conversations<wbr>Count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Number of analyzed conversations for which no issue was applicable at this point in time.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="analyzedconversationscount_go">
<a href="#analyzedconversationscount_go" style="color: inherit; text-decoration: inherit;">Analyzed<wbr>Conversations<wbr>Count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Number of conversations the issue model has analyzed at this point in time.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="issuestats_go">
<a href="#issuestats_go" style="color: inherit; text-decoration: inherit;">Issue<wbr>Stats</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}Statistics on each issue. Key is the issue's resource name.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="unclassifiedconversationscount_go">
<a href="#unclassifiedconversationscount_go" style="color: inherit; text-decoration: inherit;">Unclassified<wbr>Conversations<wbr>Count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Number of analyzed conversations for which no issue was applicable at this point in time.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="analyzedconversationscount_nodejs">
<a href="#analyzedconversationscount_nodejs" style="color: inherit; text-decoration: inherit;">analyzed<wbr>Conversations<wbr>Count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Number of conversations the issue model has analyzed at this point in time.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="issuestats_nodejs">
<a href="#issuestats_nodejs" style="color: inherit; text-decoration: inherit;">issue<wbr>Stats</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}Statistics on each issue. Key is the issue's resource name.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="unclassifiedconversationscount_nodejs">
<a href="#unclassifiedconversationscount_nodejs" style="color: inherit; text-decoration: inherit;">unclassified<wbr>Conversations<wbr>Count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Number of analyzed conversations for which no issue was applicable at this point in time.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="analyzed_conversations_count_python">
<a href="#analyzed_conversations_count_python" style="color: inherit; text-decoration: inherit;">analyzed_<wbr>conversations_<wbr>count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Number of conversations the issue model has analyzed at this point in time.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="issue_stats_python">
<a href="#issue_stats_python" style="color: inherit; text-decoration: inherit;">issue_<wbr>stats</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}Statistics on each issue. Key is the issue's resource name.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="unclassified_conversations_count_python">
<a href="#unclassified_conversations_count_python" style="color: inherit; text-decoration: inherit;">unclassified_<wbr>conversations_<wbr>count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Number of analyzed conversations for which no issue was applicable at this point in time.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-google-native">https://github.com/pulumi/pulumi-google-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
