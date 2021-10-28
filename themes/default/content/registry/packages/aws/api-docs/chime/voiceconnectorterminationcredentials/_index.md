
---
title: "VoiceConnectorTerminationCredentials"
title_tag: "aws.chime.VoiceConnectorTerminationCredentials"
meta_desc: "Documentation for the aws.chime.VoiceConnectorTerminationCredentials resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Adds termination SIP credentials for the specified Amazon Chime Voice Connector.

> **Note:** Voice Connector Termination Credentials requires a [Voice Connector Termination](https://www.terraform.io/docs/providers/aws/r/chime_voice_connector_termination.html) to be present. Use of `depends_on` (as shown below) is recommended to avoid race conditions.

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Aws = Pulumi.Aws;

class MyStack : Stack
{
    public MyStack()
    {
        var defaultVoiceConnector = new Aws.Chime.VoiceConnector("defaultVoiceConnector", new Aws.Chime.VoiceConnectorArgs
        {
            RequireEncryption = true,
        });
        var defaultVoiceConnectorTermination = new Aws.Chime.VoiceConnectorTermination("defaultVoiceConnectorTermination", new Aws.Chime.VoiceConnectorTerminationArgs
        {
            Disabled = true,
            CpsLimit = 1,
            CidrAllowLists = 
            {
                "50.35.78.96/31",
            },
            CallingRegions = 
            {
                "US",
                "CA",
            },
            VoiceConnectorId = defaultVoiceConnector.Id,
        });
        var defaultVoiceConnectorTerminationCredentials = new Aws.Chime.VoiceConnectorTerminationCredentials("defaultVoiceConnectorTerminationCredentials", new Aws.Chime.VoiceConnectorTerminationCredentialsArgs
        {
            VoiceConnectorId = defaultVoiceConnector.Id,
            Credentials = 
            {
                new Aws.Chime.Inputs.VoiceConnectorTerminationCredentialsCredentialArgs
                {
                    Username = "test",
                    Password = "test!",
                },
            },
        }, new CustomResourceOptions
        {
            DependsOn = 
            {
                defaultVoiceConnectorTermination,
            },
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-aws/sdk/v4/go/aws/chime"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		defaultVoiceConnector, err := chime.NewVoiceConnector(ctx, "defaultVoiceConnector", &chime.VoiceConnectorArgs{
			RequireEncryption: pulumi.Bool(true),
		})
		if err != nil {
			return err
		}
		defaultVoiceConnectorTermination, err := chime.NewVoiceConnectorTermination(ctx, "defaultVoiceConnectorTermination", &chime.VoiceConnectorTerminationArgs{
			Disabled: pulumi.Bool(true),
			CpsLimit: pulumi.Int(1),
			CidrAllowLists: pulumi.StringArray{
				pulumi.String("50.35.78.96/31"),
			},
			CallingRegions: pulumi.StringArray{
				pulumi.String("US"),
				pulumi.String("CA"),
			},
			VoiceConnectorId: defaultVoiceConnector.ID(),
		})
		if err != nil {
			return err
		}
		_, err = chime.NewVoiceConnectorTerminationCredentials(ctx, "defaultVoiceConnectorTerminationCredentials", &chime.VoiceConnectorTerminationCredentialsArgs{
			VoiceConnectorId: defaultVoiceConnector.ID(),
			Credentials: chime.VoiceConnectorTerminationCredentialsCredentialArray{
				&chime.VoiceConnectorTerminationCredentialsCredentialArgs{
					Username: pulumi.String("test"),
					Password: pulumi.String("test!"),
				},
			},
		}, pulumi.DependsOn([]pulumi.Resource{
			defaultVoiceConnectorTermination,
		}))
		if err != nil {
			return err
		}
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_aws as aws

default_voice_connector = aws.chime.VoiceConnector("defaultVoiceConnector", require_encryption=True)
default_voice_connector_termination = aws.chime.VoiceConnectorTermination("defaultVoiceConnectorTermination",
    disabled=True,
    cps_limit=1,
    cidr_allow_lists=["50.35.78.96/31"],
    calling_regions=[
        "US",
        "CA",
    ],
    voice_connector_id=default_voice_connector.id)
default_voice_connector_termination_credentials = aws.chime.VoiceConnectorTerminationCredentials("defaultVoiceConnectorTerminationCredentials",
    voice_connector_id=default_voice_connector.id,
    credentials=[aws.chime.VoiceConnectorTerminationCredentialsCredentialArgs(
        username="test",
        password="test!",
    )],
    opts=pulumi.ResourceOptions(depends_on=[default_voice_connector_termination]))
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const defaultVoiceConnector = new aws.chime.VoiceConnector("defaultVoiceConnector", {requireEncryption: true});
const defaultVoiceConnectorTermination = new aws.chime.VoiceConnectorTermination("defaultVoiceConnectorTermination", {
    disabled: true,
    cpsLimit: 1,
    cidrAllowLists: ["50.35.78.96/31"],
    callingRegions: [
        "US",
        "CA",
    ],
    voiceConnectorId: defaultVoiceConnector.id,
});
const defaultVoiceConnectorTerminationCredentials = new aws.chime.VoiceConnectorTerminationCredentials("defaultVoiceConnectorTerminationCredentials", {
    voiceConnectorId: defaultVoiceConnector.id,
    credentials: [{
        username: "test",
        password: "test!",
    }],
}, {
    dependsOn: [defaultVoiceConnectorTermination],
});
```


{{< /example >}}





{{% /examples %}}




## Create a VoiceConnectorTerminationCredentials Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">VoiceConnectorTerminationCredentials</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">VoiceConnectorTerminationCredentialsArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">VoiceConnectorTerminationCredentials</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                                         <span class="nx">credentials</span><span class="p">:</span> <span class="nx">Optional[Sequence[VoiceConnectorTerminationCredentialsCredentialArgs]]</span> = None<span class="p">,</span>
                                         <span class="nx">voice_connector_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">VoiceConnectorTerminationCredentials</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                         <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">VoiceConnectorTerminationCredentialsArgs</a></span><span class="p">,</span>
                                         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewVoiceConnectorTerminationCredentials</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">VoiceConnectorTerminationCredentialsArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">VoiceConnectorTerminationCredentials</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">VoiceConnectorTerminationCredentials</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">VoiceConnectorTerminationCredentialsArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">VoiceConnectorTerminationCredentialsArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language python %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">VoiceConnectorTerminationCredentialsArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">ResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties"><dt
        class="property-optional" title="Optional">
        <span>ctx</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span>
    </dt>
    <dd>Context object for the current deployment.</dd><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">VoiceConnectorTerminationCredentialsArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">VoiceConnectorTerminationCredentialsArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## VoiceConnectorTerminationCredentials Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The VoiceConnectorTerminationCredentials resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="credentials_csharp">
<a href="#credentials_csharp" style="color: inherit; text-decoration: inherit;">Credentials</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#voiceconnectorterminationcredentialscredential">List&lt;Voice<wbr>Connector<wbr>Termination<wbr>Credentials<wbr>Credential<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}List of termination SIP credentials.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="voiceconnectorid_csharp">
<a href="#voiceconnectorid_csharp" style="color: inherit; text-decoration: inherit;">Voice<wbr>Connector<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Amazon Chime Voice Connector ID.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="credentials_go">
<a href="#credentials_go" style="color: inherit; text-decoration: inherit;">Credentials</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#voiceconnectorterminationcredentialscredential">[]Voice<wbr>Connector<wbr>Termination<wbr>Credentials<wbr>Credential<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}List of termination SIP credentials.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="voiceconnectorid_go">
<a href="#voiceconnectorid_go" style="color: inherit; text-decoration: inherit;">Voice<wbr>Connector<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Amazon Chime Voice Connector ID.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="credentials_nodejs">
<a href="#credentials_nodejs" style="color: inherit; text-decoration: inherit;">credentials</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#voiceconnectorterminationcredentialscredential">Voice<wbr>Connector<wbr>Termination<wbr>Credentials<wbr>Credential<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}List of termination SIP credentials.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="voiceconnectorid_nodejs">
<a href="#voiceconnectorid_nodejs" style="color: inherit; text-decoration: inherit;">voice<wbr>Connector<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Amazon Chime Voice Connector ID.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="credentials_python">
<a href="#credentials_python" style="color: inherit; text-decoration: inherit;">credentials</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#voiceconnectorterminationcredentialscredential">Sequence[Voice<wbr>Connector<wbr>Termination<wbr>Credentials<wbr>Credential<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}List of termination SIP credentials.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="voice_connector_id_python">
<a href="#voice_connector_id_python" style="color: inherit; text-decoration: inherit;">voice_<wbr>connector_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Amazon Chime Voice Connector ID.
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the VoiceConnectorTerminationCredentials resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}



## Look up an Existing VoiceConnectorTerminationCredentials Resource {#look-up}

Get an existing VoiceConnectorTerminationCredentials resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">VoiceConnectorTerminationCredentialsState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">VoiceConnectorTerminationCredentials</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">credentials</span><span class="p">:</span> <span class="nx">Optional[Sequence[VoiceConnectorTerminationCredentialsCredentialArgs]]</span> = None<span class="p">,</span>
        <span class="nx">voice_connector_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">) -&gt;</span> VoiceConnectorTerminationCredentials</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetVoiceConnectorTerminationCredentials<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">VoiceConnectorTerminationCredentialsState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">VoiceConnectorTerminationCredentials</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">VoiceConnectorTerminationCredentials</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">VoiceConnectorTerminationCredentialsState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_credentials_csharp">
<a href="#state_credentials_csharp" style="color: inherit; text-decoration: inherit;">Credentials</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#voiceconnectorterminationcredentialscredential">List&lt;Voice<wbr>Connector<wbr>Termination<wbr>Credentials<wbr>Credential<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}List of termination SIP credentials.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_voiceconnectorid_csharp">
<a href="#state_voiceconnectorid_csharp" style="color: inherit; text-decoration: inherit;">Voice<wbr>Connector<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Amazon Chime Voice Connector ID.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_credentials_go">
<a href="#state_credentials_go" style="color: inherit; text-decoration: inherit;">Credentials</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#voiceconnectorterminationcredentialscredential">[]Voice<wbr>Connector<wbr>Termination<wbr>Credentials<wbr>Credential<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}List of termination SIP credentials.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_voiceconnectorid_go">
<a href="#state_voiceconnectorid_go" style="color: inherit; text-decoration: inherit;">Voice<wbr>Connector<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Amazon Chime Voice Connector ID.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_credentials_nodejs">
<a href="#state_credentials_nodejs" style="color: inherit; text-decoration: inherit;">credentials</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#voiceconnectorterminationcredentialscredential">Voice<wbr>Connector<wbr>Termination<wbr>Credentials<wbr>Credential<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}List of termination SIP credentials.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_voiceconnectorid_nodejs">
<a href="#state_voiceconnectorid_nodejs" style="color: inherit; text-decoration: inherit;">voice<wbr>Connector<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Amazon Chime Voice Connector ID.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_credentials_python">
<a href="#state_credentials_python" style="color: inherit; text-decoration: inherit;">credentials</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#voiceconnectorterminationcredentialscredential">Sequence[Voice<wbr>Connector<wbr>Termination<wbr>Credentials<wbr>Credential<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}List of termination SIP credentials.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_voice_connector_id_python">
<a href="#state_voice_connector_id_python" style="color: inherit; text-decoration: inherit;">voice_<wbr>connector_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Amazon Chime Voice Connector ID.
{{% /md %}}</dd></dl>
{{% /choosable %}}






## Supporting Types



<h4 id="voiceconnectorterminationcredentialscredential">Voice<wbr>Connector<wbr>Termination<wbr>Credentials<wbr>Credential</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="password_csharp">
<a href="#password_csharp" style="color: inherit; text-decoration: inherit;">Password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}RFC2617 compliant password associated with the SIP credentials.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="username_csharp">
<a href="#username_csharp" style="color: inherit; text-decoration: inherit;">Username</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}RFC2617 compliant username associated with the SIP credentials.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="password_go">
<a href="#password_go" style="color: inherit; text-decoration: inherit;">Password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}RFC2617 compliant password associated with the SIP credentials.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="username_go">
<a href="#username_go" style="color: inherit; text-decoration: inherit;">Username</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}RFC2617 compliant username associated with the SIP credentials.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="password_nodejs">
<a href="#password_nodejs" style="color: inherit; text-decoration: inherit;">password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}RFC2617 compliant password associated with the SIP credentials.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="username_nodejs">
<a href="#username_nodejs" style="color: inherit; text-decoration: inherit;">username</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}RFC2617 compliant username associated with the SIP credentials.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="password_python">
<a href="#password_python" style="color: inherit; text-decoration: inherit;">password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}RFC2617 compliant password associated with the SIP credentials.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="username_python">
<a href="#username_python" style="color: inherit; text-decoration: inherit;">username</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}RFC2617 compliant username associated with the SIP credentials.
{{% /md %}}</dd></dl>
{{% /choosable %}}
## Import


Chime Voice Connector Termination Credentials can be imported using the `voice_connector_id`, e.g.

```sh
 $ pulumi import aws:chime/voiceConnectorTerminationCredentials:VoiceConnectorTerminationCredentials default abcdef1ghij2klmno3pqr4
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws">https://github.com/pulumi/pulumi-aws</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`aws` Terraform Provider](https://github.com/terraform-providers/terraform-provider-aws).{{% /md %}}</dd>
</dl>
