
---
title: "getCiphertext"
title_tag: "alicloud.kms.getCiphertext"
meta_desc: "Documentation for the alicloud.kms.getCiphertext function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->




## Using getCiphertext {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getCiphertext<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetCiphertextArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetCiphertextResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_ciphertext(</span><span class="nx">encryption_context</span><span class="p">:</span> <span class="nx">Optional[Mapping[str, str]]</span> = None<span class="p">,</span>
                   <span class="nx">key_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                   <span class="nx">plaintext</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                   <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetCiphertextResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupCiphertext<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupCiphertextArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupCiphertextResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupCiphertext` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetCiphertext </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetCiphertextResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetCiphertextArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="keyid_csharp">
<a href="#keyid_csharp" style="color: inherit; text-decoration: inherit;">Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The globally unique ID of the CMK.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="plaintext_csharp">
<a href="#plaintext_csharp" style="color: inherit; text-decoration: inherit;">Plaintext</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The plaintext to be encrypted which must be encoded in Base64.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="encryptioncontext_csharp">
<a href="#encryptioncontext_csharp" style="color: inherit; text-decoration: inherit;">Encryption<wbr>Context</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}-
(Optional) The Encryption context. If you specify this parameter here, it is also required when you call the Decrypt API operation. For more information, see [Encryption Context](https://www.alibabacloud.com/help/doc-detail/42975.htm).
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="keyid_go">
<a href="#keyid_go" style="color: inherit; text-decoration: inherit;">Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The globally unique ID of the CMK.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="plaintext_go">
<a href="#plaintext_go" style="color: inherit; text-decoration: inherit;">Plaintext</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The plaintext to be encrypted which must be encoded in Base64.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="encryptioncontext_go">
<a href="#encryptioncontext_go" style="color: inherit; text-decoration: inherit;">Encryption<wbr>Context</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}-
(Optional) The Encryption context. If you specify this parameter here, it is also required when you call the Decrypt API operation. For more information, see [Encryption Context](https://www.alibabacloud.com/help/doc-detail/42975.htm).
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="keyid_nodejs">
<a href="#keyid_nodejs" style="color: inherit; text-decoration: inherit;">key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The globally unique ID of the CMK.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="plaintext_nodejs">
<a href="#plaintext_nodejs" style="color: inherit; text-decoration: inherit;">plaintext</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The plaintext to be encrypted which must be encoded in Base64.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="encryptioncontext_nodejs">
<a href="#encryptioncontext_nodejs" style="color: inherit; text-decoration: inherit;">encryption<wbr>Context</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}-
(Optional) The Encryption context. If you specify this parameter here, it is also required when you call the Decrypt API operation. For more information, see [Encryption Context](https://www.alibabacloud.com/help/doc-detail/42975.htm).
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_id_python">
<a href="#key_id_python" style="color: inherit; text-decoration: inherit;">key_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The globally unique ID of the CMK.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="plaintext_python">
<a href="#plaintext_python" style="color: inherit; text-decoration: inherit;">plaintext</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The plaintext to be encrypted which must be encoded in Base64.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="encryption_context_python">
<a href="#encryption_context_python" style="color: inherit; text-decoration: inherit;">encryption_<wbr>context</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}-
(Optional) The Encryption context. If you specify this parameter here, it is also required when you call the Decrypt API operation. For more information, see [Encryption Context](https://www.alibabacloud.com/help/doc-detail/42975.htm).
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getCiphertext Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="ciphertextblob_csharp">
<a href="#ciphertextblob_csharp" style="color: inherit; text-decoration: inherit;">Ciphertext<wbr>Blob</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ciphertext of the data key encrypted with the primary CMK version.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="keyid_csharp">
<a href="#keyid_csharp" style="color: inherit; text-decoration: inherit;">Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="plaintext_csharp">
<a href="#plaintext_csharp" style="color: inherit; text-decoration: inherit;">Plaintext</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="encryptioncontext_csharp">
<a href="#encryptioncontext_csharp" style="color: inherit; text-decoration: inherit;">Encryption<wbr>Context</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="ciphertextblob_go">
<a href="#ciphertextblob_go" style="color: inherit; text-decoration: inherit;">Ciphertext<wbr>Blob</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ciphertext of the data key encrypted with the primary CMK version.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="keyid_go">
<a href="#keyid_go" style="color: inherit; text-decoration: inherit;">Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="plaintext_go">
<a href="#plaintext_go" style="color: inherit; text-decoration: inherit;">Plaintext</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="encryptioncontext_go">
<a href="#encryptioncontext_go" style="color: inherit; text-decoration: inherit;">Encryption<wbr>Context</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="ciphertextblob_nodejs">
<a href="#ciphertextblob_nodejs" style="color: inherit; text-decoration: inherit;">ciphertext<wbr>Blob</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ciphertext of the data key encrypted with the primary CMK version.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="keyid_nodejs">
<a href="#keyid_nodejs" style="color: inherit; text-decoration: inherit;">key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="plaintext_nodejs">
<a href="#plaintext_nodejs" style="color: inherit; text-decoration: inherit;">plaintext</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="encryptioncontext_nodejs">
<a href="#encryptioncontext_nodejs" style="color: inherit; text-decoration: inherit;">encryption<wbr>Context</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="ciphertext_blob_python">
<a href="#ciphertext_blob_python" style="color: inherit; text-decoration: inherit;">ciphertext_<wbr>blob</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ciphertext of the data key encrypted with the primary CMK version.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="key_id_python">
<a href="#key_id_python" style="color: inherit; text-decoration: inherit;">key_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="plaintext_python">
<a href="#plaintext_python" style="color: inherit; text-decoration: inherit;">plaintext</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="encryption_context_python">
<a href="#encryption_context_python" style="color: inherit; text-decoration: inherit;">encryption_<wbr>context</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-alicloud">https://github.com/pulumi/pulumi-alicloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`alicloud` Terraform Provider](https://github.com/aliyun/terraform-provider-alicloud).{{% /md %}}</dd>
</dl>
