
---
title: "getKeyVersions"
title_tag: "alicloud.kms.getKeyVersions"
meta_desc: "Documentation for the alicloud.kms.getKeyVersions function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

This data source provides a list of KMS KeyVersions in an Alibaba Cloud account according to the specified filters.

> NOTE: Available in v1.85.0+


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using AliCloud = Pulumi.AliCloud;

class MyStack : Stack
{
    public MyStack()
    {
        var alicloudKmsKeyVersionsDs = Output.Create(AliCloud.Kms.GetKeyVersions.InvokeAsync(new AliCloud.Kms.GetKeyVersionsArgs
        {
            Ids = 
            {
                "d89e8a53-b708-41aa-8c67-6873axxx",
            },
            KeyId = "08438c-b4d5-4d05-928c-07b7xxxx",
        }));
        this.AllVersions = alicloudKmsKeyVersionsDs.Apply(alicloudKmsKeyVersionsDs => alicloudKmsKeyVersionsDs.Versions);
    }

    [Output("allVersions")]
    public Output<string> AllVersions { get; set; }
}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-alicloud/sdk/v3/go/alicloud/kms"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		alicloudKmsKeyVersionsDs, err := kms.GetKeyVersions(ctx, &kms.GetKeyVersionsArgs{
			Ids: []string{
				"d89e8a53-b708-41aa-8c67-6873axxx",
			},
			KeyId: "08438c-b4d5-4d05-928c-07b7xxxx",
		}, nil)
		if err != nil {
			return err
		}
		ctx.Export("allVersions", alicloudKmsKeyVersionsDs.Versions)
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_alicloud as alicloud

alicloud_kms_key_versions_ds = alicloud.kms.get_key_versions(ids=["d89e8a53-b708-41aa-8c67-6873axxx"],
    key_id="08438c-b4d5-4d05-928c-07b7xxxx")
pulumi.export("allVersions", alicloud_kms_key_versions_ds.versions)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

// Declare the data source
const alicloudKmsKeyVersionsDs = pulumi.output(alicloud.kms.getKeyVersions({
    ids: ["d89e8a53-b708-41aa-8c67-6873axxx"],
    keyId: "08438c-b4d5-4d05-928c-07b7xxxx",
}, { async: true }));

export const allVersions = alicloudKmsKeyVersionsDs.versions;
```


{{< /example >}}





{{% /examples %}}




## Using getKeyVersions {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getKeyVersions<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetKeyVersionsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetKeyVersionsResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_key_versions(</span><span class="nx">ids</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
                     <span class="nx">key_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                     <span class="nx">output_file</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                     <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetKeyVersionsResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetKeyVersions<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetKeyVersionsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetKeyVersionsResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetKeyVersions` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetKeyVersions </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetKeyVersionsResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetKeyVersionsArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
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
    <dd>{{% md %}}The id of kms key.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="ids_csharp">
<a href="#ids_csharp" style="color: inherit; text-decoration: inherit;">Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of KMS KeyVersion IDs.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_csharp">
<a href="#outputfile_csharp" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The id of kms key.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="ids_go">
<a href="#ids_go" style="color: inherit; text-decoration: inherit;">Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of KMS KeyVersion IDs.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_go">
<a href="#outputfile_go" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The id of kms key.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="ids_nodejs">
<a href="#ids_nodejs" style="color: inherit; text-decoration: inherit;">ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of KMS KeyVersion IDs.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_nodejs">
<a href="#outputfile_nodejs" style="color: inherit; text-decoration: inherit;">output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The id of kms key.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="ids_python">
<a href="#ids_python" style="color: inherit; text-decoration: inherit;">ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of KMS KeyVersion IDs.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="output_file_python">
<a href="#output_file_python" style="color: inherit; text-decoration: inherit;">output_<wbr>file</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## getKeyVersions Result {#result}

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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ids_csharp">
<a href="#ids_csharp" style="color: inherit; text-decoration: inherit;">Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of KMS KeyVersion IDs.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="keyid_csharp">
<a href="#keyid_csharp" style="color: inherit; text-decoration: inherit;">Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the key.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versions_csharp">
<a href="#versions_csharp" style="color: inherit; text-decoration: inherit;">Versions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkeyversionsversion">List&lt;Pulumi.<wbr>Ali<wbr>Cloud.<wbr>Kms.<wbr>Outputs.<wbr>Get<wbr>Key<wbr>Versions<wbr>Version&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of KMS KeyVersions. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_csharp">
<a href="#outputfile_csharp" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ids_go">
<a href="#ids_go" style="color: inherit; text-decoration: inherit;">Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of KMS KeyVersion IDs.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="keyid_go">
<a href="#keyid_go" style="color: inherit; text-decoration: inherit;">Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the key.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versions_go">
<a href="#versions_go" style="color: inherit; text-decoration: inherit;">Versions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkeyversionsversion">[]Get<wbr>Key<wbr>Versions<wbr>Version</a></span>
    </dt>
    <dd>{{% md %}}A list of KMS KeyVersions. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_go">
<a href="#outputfile_go" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ids_nodejs">
<a href="#ids_nodejs" style="color: inherit; text-decoration: inherit;">ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of KMS KeyVersion IDs.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="keyid_nodejs">
<a href="#keyid_nodejs" style="color: inherit; text-decoration: inherit;">key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the key.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versions_nodejs">
<a href="#versions_nodejs" style="color: inherit; text-decoration: inherit;">versions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkeyversionsversion">Get<wbr>Key<wbr>Versions<wbr>Version[]</a></span>
    </dt>
    <dd>{{% md %}}A list of KMS KeyVersions. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_nodejs">
<a href="#outputfile_nodejs" style="color: inherit; text-decoration: inherit;">output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ids_python">
<a href="#ids_python" style="color: inherit; text-decoration: inherit;">ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of KMS KeyVersion IDs.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="key_id_python">
<a href="#key_id_python" style="color: inherit; text-decoration: inherit;">key_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the key.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="versions_python">
<a href="#versions_python" style="color: inherit; text-decoration: inherit;">versions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkeyversionsversion">Sequence[Get<wbr>Key<wbr>Versions<wbr>Version]</a></span>
    </dt>
    <dd>{{% md %}}A list of KMS KeyVersions. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="output_file_python">
<a href="#output_file_python" style="color: inherit; text-decoration: inherit;">output_<wbr>file</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getkeyversionsversion">Get<wbr>Key<wbr>Versions<wbr>Version</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="createtime_csharp">
<a href="#createtime_csharp" style="color: inherit; text-decoration: inherit;">Create<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Date and time when the key version was created (UTC time).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="creationdate_csharp">
<a href="#creationdate_csharp" style="color: inherit; text-decoration: inherit;">Creation<wbr>Date</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Removed from v1.124.4) It has been removed and using `create_time` instead.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the KMS KeyVersion resource.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="keyid_csharp">
<a href="#keyid_csharp" style="color: inherit; text-decoration: inherit;">Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of kms key.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="keyversionid_csharp">
<a href="#keyversionid_csharp" style="color: inherit; text-decoration: inherit;">Key<wbr>Version<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the key version.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="createtime_go">
<a href="#createtime_go" style="color: inherit; text-decoration: inherit;">Create<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Date and time when the key version was created (UTC time).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="creationdate_go">
<a href="#creationdate_go" style="color: inherit; text-decoration: inherit;">Creation<wbr>Date</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Removed from v1.124.4) It has been removed and using `create_time` instead.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the KMS KeyVersion resource.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="keyid_go">
<a href="#keyid_go" style="color: inherit; text-decoration: inherit;">Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of kms key.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="keyversionid_go">
<a href="#keyversionid_go" style="color: inherit; text-decoration: inherit;">Key<wbr>Version<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the key version.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="createtime_nodejs">
<a href="#createtime_nodejs" style="color: inherit; text-decoration: inherit;">create<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Date and time when the key version was created (UTC time).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="creationdate_nodejs">
<a href="#creationdate_nodejs" style="color: inherit; text-decoration: inherit;">creation<wbr>Date</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Removed from v1.124.4) It has been removed and using `create_time` instead.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the KMS KeyVersion resource.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="keyid_nodejs">
<a href="#keyid_nodejs" style="color: inherit; text-decoration: inherit;">key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of kms key.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="keyversionid_nodejs">
<a href="#keyversionid_nodejs" style="color: inherit; text-decoration: inherit;">key<wbr>Version<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the key version.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="create_time_python">
<a href="#create_time_python" style="color: inherit; text-decoration: inherit;">create_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Date and time when the key version was created (UTC time).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="creation_date_python">
<a href="#creation_date_python" style="color: inherit; text-decoration: inherit;">creation_<wbr>date</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Removed from v1.124.4) It has been removed and using `create_time` instead.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the KMS KeyVersion resource.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="key_id_python">
<a href="#key_id_python" style="color: inherit; text-decoration: inherit;">key_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The id of kms key.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="key_version_id_python">
<a href="#key_version_id_python" style="color: inherit; text-decoration: inherit;">key_<wbr>version_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the key version.
{{% /md %}}</dd></dl>
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
