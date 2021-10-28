
---
title: "getConsentArtifact"
title_tag: "google-native.healthcare/v1.getConsentArtifact"
meta_desc: "Documentation for the google-native.healthcare/v1.getConsentArtifact function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Gets the specified Consent artifact.




## Using getConsentArtifact {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getConsentArtifact<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetConsentArtifactArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetConsentArtifactResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_consent_artifact(</span><span class="nx">consent_artifact_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">consent_store_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">dataset_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">location</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">project</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetConsentArtifactResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupConsentArtifact<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupConsentArtifactArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupConsentArtifactResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupConsentArtifact` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetConsentArtifact </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetConsentArtifactResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetConsentArtifactArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="consentartifactid_csharp">
<a href="#consentartifactid_csharp" style="color: inherit; text-decoration: inherit;">Consent<wbr>Artifact<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="consentstoreid_csharp">
<a href="#consentstoreid_csharp" style="color: inherit; text-decoration: inherit;">Consent<wbr>Store<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="datasetid_csharp">
<a href="#datasetid_csharp" style="color: inherit; text-decoration: inherit;">Dataset<wbr>Id</a>
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
        <span id="consentartifactid_go">
<a href="#consentartifactid_go" style="color: inherit; text-decoration: inherit;">Consent<wbr>Artifact<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="consentstoreid_go">
<a href="#consentstoreid_go" style="color: inherit; text-decoration: inherit;">Consent<wbr>Store<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="datasetid_go">
<a href="#datasetid_go" style="color: inherit; text-decoration: inherit;">Dataset<wbr>Id</a>
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
        <span id="consentartifactid_nodejs">
<a href="#consentartifactid_nodejs" style="color: inherit; text-decoration: inherit;">consent<wbr>Artifact<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="consentstoreid_nodejs">
<a href="#consentstoreid_nodejs" style="color: inherit; text-decoration: inherit;">consent<wbr>Store<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="datasetid_nodejs">
<a href="#datasetid_nodejs" style="color: inherit; text-decoration: inherit;">dataset<wbr>Id</a>
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
        <span id="consent_artifact_id_python">
<a href="#consent_artifact_id_python" style="color: inherit; text-decoration: inherit;">consent_<wbr>artifact_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="consent_store_id_python">
<a href="#consent_store_id_python" style="color: inherit; text-decoration: inherit;">consent_<wbr>store_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="dataset_id_python">
<a href="#dataset_id_python" style="color: inherit; text-decoration: inherit;">dataset_<wbr>id</a>
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




## getConsentArtifact Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="consentcontentscreenshots_csharp">
<a href="#consentcontentscreenshots_csharp" style="color: inherit; text-decoration: inherit;">Consent<wbr>Content<wbr>Screenshots</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#imageresponse">List&lt;Pulumi.<wbr>Google<wbr>Native.<wbr>Healthcare.<wbr>V1.<wbr>Outputs.<wbr>Image<wbr>Response&gt;</a></span>
    </dt>
    <dd>{{% md %}}Optional. Screenshots, PDFs, or other binary information documenting the user's consent.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="consentcontentversion_csharp">
<a href="#consentcontentversion_csharp" style="color: inherit; text-decoration: inherit;">Consent<wbr>Content<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. An string indicating the version of the consent information shown to the user.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="guardiansignature_csharp">
<a href="#guardiansignature_csharp" style="color: inherit; text-decoration: inherit;">Guardian<wbr>Signature</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#signatureresponse">Pulumi.<wbr>Google<wbr>Native.<wbr>Healthcare.<wbr>V1.<wbr>Outputs.<wbr>Signature<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. A signature from a guardian.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="metadata_csharp">
<a href="#metadata_csharp" style="color: inherit; text-decoration: inherit;">Metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}Optional. Metadata associated with the Consent artifact. For example, the consent locale or user agent version.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name of the Consent artifact, of the form `projects/{project_id}/locations/{location_id}/datasets/{dataset_id}/consentStores/{consent_store_id}/consentArtifacts/{consent_artifact_id}`. Cannot be changed after creation.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="userid_csharp">
<a href="#userid_csharp" style="color: inherit; text-decoration: inherit;">User<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}User's UUID provided by the client.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="usersignature_csharp">
<a href="#usersignature_csharp" style="color: inherit; text-decoration: inherit;">User<wbr>Signature</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#signatureresponse">Pulumi.<wbr>Google<wbr>Native.<wbr>Healthcare.<wbr>V1.<wbr>Outputs.<wbr>Signature<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. User's signature.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="witnesssignature_csharp">
<a href="#witnesssignature_csharp" style="color: inherit; text-decoration: inherit;">Witness<wbr>Signature</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#signatureresponse">Pulumi.<wbr>Google<wbr>Native.<wbr>Healthcare.<wbr>V1.<wbr>Outputs.<wbr>Signature<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. A signature from a witness.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="consentcontentscreenshots_go">
<a href="#consentcontentscreenshots_go" style="color: inherit; text-decoration: inherit;">Consent<wbr>Content<wbr>Screenshots</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#imageresponse">[]Image<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. Screenshots, PDFs, or other binary information documenting the user's consent.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="consentcontentversion_go">
<a href="#consentcontentversion_go" style="color: inherit; text-decoration: inherit;">Consent<wbr>Content<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. An string indicating the version of the consent information shown to the user.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="guardiansignature_go">
<a href="#guardiansignature_go" style="color: inherit; text-decoration: inherit;">Guardian<wbr>Signature</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#signatureresponse">Signature<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. A signature from a guardian.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="metadata_go">
<a href="#metadata_go" style="color: inherit; text-decoration: inherit;">Metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}Optional. Metadata associated with the Consent artifact. For example, the consent locale or user agent version.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name of the Consent artifact, of the form `projects/{project_id}/locations/{location_id}/datasets/{dataset_id}/consentStores/{consent_store_id}/consentArtifacts/{consent_artifact_id}`. Cannot be changed after creation.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="userid_go">
<a href="#userid_go" style="color: inherit; text-decoration: inherit;">User<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}User's UUID provided by the client.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="usersignature_go">
<a href="#usersignature_go" style="color: inherit; text-decoration: inherit;">User<wbr>Signature</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#signatureresponse">Signature<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. User's signature.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="witnesssignature_go">
<a href="#witnesssignature_go" style="color: inherit; text-decoration: inherit;">Witness<wbr>Signature</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#signatureresponse">Signature<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. A signature from a witness.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="consentcontentscreenshots_nodejs">
<a href="#consentcontentscreenshots_nodejs" style="color: inherit; text-decoration: inherit;">consent<wbr>Content<wbr>Screenshots</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#imageresponse">Image<wbr>Response[]</a></span>
    </dt>
    <dd>{{% md %}}Optional. Screenshots, PDFs, or other binary information documenting the user's consent.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="consentcontentversion_nodejs">
<a href="#consentcontentversion_nodejs" style="color: inherit; text-decoration: inherit;">consent<wbr>Content<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. An string indicating the version of the consent information shown to the user.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="guardiansignature_nodejs">
<a href="#guardiansignature_nodejs" style="color: inherit; text-decoration: inherit;">guardian<wbr>Signature</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#signatureresponse">Signature<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. A signature from a guardian.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="metadata_nodejs">
<a href="#metadata_nodejs" style="color: inherit; text-decoration: inherit;">metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}Optional. Metadata associated with the Consent artifact. For example, the consent locale or user agent version.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name of the Consent artifact, of the form `projects/{project_id}/locations/{location_id}/datasets/{dataset_id}/consentStores/{consent_store_id}/consentArtifacts/{consent_artifact_id}`. Cannot be changed after creation.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="userid_nodejs">
<a href="#userid_nodejs" style="color: inherit; text-decoration: inherit;">user<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}User's UUID provided by the client.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="usersignature_nodejs">
<a href="#usersignature_nodejs" style="color: inherit; text-decoration: inherit;">user<wbr>Signature</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#signatureresponse">Signature<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. User's signature.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="witnesssignature_nodejs">
<a href="#witnesssignature_nodejs" style="color: inherit; text-decoration: inherit;">witness<wbr>Signature</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#signatureresponse">Signature<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. A signature from a witness.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="consent_content_screenshots_python">
<a href="#consent_content_screenshots_python" style="color: inherit; text-decoration: inherit;">consent_<wbr>content_<wbr>screenshots</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#imageresponse">Sequence[Image<wbr>Response]</a></span>
    </dt>
    <dd>{{% md %}}Optional. Screenshots, PDFs, or other binary information documenting the user's consent.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="consent_content_version_python">
<a href="#consent_content_version_python" style="color: inherit; text-decoration: inherit;">consent_<wbr>content_<wbr>version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Optional. An string indicating the version of the consent information shown to the user.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="guardian_signature_python">
<a href="#guardian_signature_python" style="color: inherit; text-decoration: inherit;">guardian_<wbr>signature</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#signatureresponse">Signature<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. A signature from a guardian.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="metadata_python">
<a href="#metadata_python" style="color: inherit; text-decoration: inherit;">metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}Optional. Metadata associated with the Consent artifact. For example, the consent locale or user agent version.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource name of the Consent artifact, of the form `projects/{project_id}/locations/{location_id}/datasets/{dataset_id}/consentStores/{consent_store_id}/consentArtifacts/{consent_artifact_id}`. Cannot be changed after creation.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="user_id_python">
<a href="#user_id_python" style="color: inherit; text-decoration: inherit;">user_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}User's UUID provided by the client.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="user_signature_python">
<a href="#user_signature_python" style="color: inherit; text-decoration: inherit;">user_<wbr>signature</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#signatureresponse">Signature<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. User's signature.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="witness_signature_python">
<a href="#witness_signature_python" style="color: inherit; text-decoration: inherit;">witness_<wbr>signature</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#signatureresponse">Signature<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. A signature from a witness.{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="imageresponse">Image<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gcsuri_csharp">
<a href="#gcsuri_csharp" style="color: inherit; text-decoration: inherit;">Gcs<wbr>Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Input only. Points to a Cloud Storage URI containing the consent artifact content. The URI must be in the following format: `gs://{bucket_id}/{object_id}`. The Cloud Healthcare API service account must have the `roles/storage.objectViewer` Cloud IAM role for this Cloud Storage location. The consent artifact content at this URI is copied to a Cloud Storage location managed by the Cloud Healthcare API. Responses to fetching requests return the consent artifact content in raw_bytes.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rawbytes_csharp">
<a href="#rawbytes_csharp" style="color: inherit; text-decoration: inherit;">Raw<wbr>Bytes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Consent artifact content represented as a stream of bytes. This field is populated when returned in GetConsentArtifact response, but not included in CreateConsentArtifact and ListConsentArtifact response.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gcsuri_go">
<a href="#gcsuri_go" style="color: inherit; text-decoration: inherit;">Gcs<wbr>Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Input only. Points to a Cloud Storage URI containing the consent artifact content. The URI must be in the following format: `gs://{bucket_id}/{object_id}`. The Cloud Healthcare API service account must have the `roles/storage.objectViewer` Cloud IAM role for this Cloud Storage location. The consent artifact content at this URI is copied to a Cloud Storage location managed by the Cloud Healthcare API. Responses to fetching requests return the consent artifact content in raw_bytes.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rawbytes_go">
<a href="#rawbytes_go" style="color: inherit; text-decoration: inherit;">Raw<wbr>Bytes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Consent artifact content represented as a stream of bytes. This field is populated when returned in GetConsentArtifact response, but not included in CreateConsentArtifact and ListConsentArtifact response.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gcsuri_nodejs">
<a href="#gcsuri_nodejs" style="color: inherit; text-decoration: inherit;">gcs<wbr>Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Input only. Points to a Cloud Storage URI containing the consent artifact content. The URI must be in the following format: `gs://{bucket_id}/{object_id}`. The Cloud Healthcare API service account must have the `roles/storage.objectViewer` Cloud IAM role for this Cloud Storage location. The consent artifact content at this URI is copied to a Cloud Storage location managed by the Cloud Healthcare API. Responses to fetching requests return the consent artifact content in raw_bytes.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rawbytes_nodejs">
<a href="#rawbytes_nodejs" style="color: inherit; text-decoration: inherit;">raw<wbr>Bytes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Consent artifact content represented as a stream of bytes. This field is populated when returned in GetConsentArtifact response, but not included in CreateConsentArtifact and ListConsentArtifact response.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gcs_uri_python">
<a href="#gcs_uri_python" style="color: inherit; text-decoration: inherit;">gcs_<wbr>uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Input only. Points to a Cloud Storage URI containing the consent artifact content. The URI must be in the following format: `gs://{bucket_id}/{object_id}`. The Cloud Healthcare API service account must have the `roles/storage.objectViewer` Cloud IAM role for this Cloud Storage location. The consent artifact content at this URI is copied to a Cloud Storage location managed by the Cloud Healthcare API. Responses to fetching requests return the consent artifact content in raw_bytes.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="raw_bytes_python">
<a href="#raw_bytes_python" style="color: inherit; text-decoration: inherit;">raw_<wbr>bytes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Consent artifact content represented as a stream of bytes. This field is populated when returned in GetConsentArtifact response, but not included in CreateConsentArtifact and ListConsentArtifact response.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="signatureresponse">Signature<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="image_csharp">
<a href="#image_csharp" style="color: inherit; text-decoration: inherit;">Image</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#imageresponse">Pulumi.<wbr>Google<wbr>Native.<wbr>Healthcare.<wbr>V1.<wbr>Inputs.<wbr>Image<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. An image of the user's signature.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="metadata_csharp">
<a href="#metadata_csharp" style="color: inherit; text-decoration: inherit;">Metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}Optional. Metadata associated with the user's signature. For example, the user's name or the user's title.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="signaturetime_csharp">
<a href="#signaturetime_csharp" style="color: inherit; text-decoration: inherit;">Signature<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. Timestamp of the signature.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="userid_csharp">
<a href="#userid_csharp" style="color: inherit; text-decoration: inherit;">User<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}User's UUID provided by the client.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="image_go">
<a href="#image_go" style="color: inherit; text-decoration: inherit;">Image</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#imageresponse">Image<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. An image of the user's signature.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="metadata_go">
<a href="#metadata_go" style="color: inherit; text-decoration: inherit;">Metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}Optional. Metadata associated with the user's signature. For example, the user's name or the user's title.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="signaturetime_go">
<a href="#signaturetime_go" style="color: inherit; text-decoration: inherit;">Signature<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. Timestamp of the signature.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="userid_go">
<a href="#userid_go" style="color: inherit; text-decoration: inherit;">User<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}User's UUID provided by the client.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="image_nodejs">
<a href="#image_nodejs" style="color: inherit; text-decoration: inherit;">image</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#imageresponse">Image<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. An image of the user's signature.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="metadata_nodejs">
<a href="#metadata_nodejs" style="color: inherit; text-decoration: inherit;">metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}Optional. Metadata associated with the user's signature. For example, the user's name or the user's title.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="signaturetime_nodejs">
<a href="#signaturetime_nodejs" style="color: inherit; text-decoration: inherit;">signature<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. Timestamp of the signature.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="userid_nodejs">
<a href="#userid_nodejs" style="color: inherit; text-decoration: inherit;">user<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}User's UUID provided by the client.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="image_python">
<a href="#image_python" style="color: inherit; text-decoration: inherit;">image</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#imageresponse">Image<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Optional. An image of the user's signature.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="metadata_python">
<a href="#metadata_python" style="color: inherit; text-decoration: inherit;">metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}Optional. Metadata associated with the user's signature. For example, the user's name or the user's title.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="signature_time_python">
<a href="#signature_time_python" style="color: inherit; text-decoration: inherit;">signature_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Optional. Timestamp of the signature.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="user_id_python">
<a href="#user_id_python" style="color: inherit; text-decoration: inherit;">user_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}User's UUID provided by the client.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-google-native">https://github.com/pulumi/pulumi-google-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
