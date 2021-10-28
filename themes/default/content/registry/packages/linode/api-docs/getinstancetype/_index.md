
---
title: "getInstanceType"
title_tag: "linode.getInstanceType"
meta_desc: "Documentation for the linode.getInstanceType function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Provides information about a Linode instance type
## Attributes

The Linode Instance Type resource exports the following attributes:

* `id` - The ID representing the Linode Type

* `label` - The Linode Type's label is for display purposes only

* `class` - The class of the Linode Type. See all classes [here](https://www.linode.com/docs/api/linode-types/#type-view__responses).

* `disk` - The Disk size, in MB, of the Linode Type

* `price.0.hourly` -  Cost (in US dollars) per hour.

* `price.0.monthly` - Cost (in US dollars) per month.

* `addons.0.backups.0.price.0.hourly` - The cost (in US dollars) per hour to add Backups service.

* `addons.0.backups.0.price.0.monthly` - The cost (in US dollars) per month to add Backups service.

* `network_out` - The Mbits outbound bandwidth allocation.

* `memory` - The amount of RAM included in this Linode Type.

* `transfer` - The monthly outbound transfer amount, in MB.

* `vcpus` - The number of VCPU cores this Linode Type offers.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Linode = Pulumi.Linode;

class MyStack : Stack
{
    public MyStack()
    {
        var @default = Output.Create(Linode.GetInstanceType.InvokeAsync(new Linode.GetInstanceTypeArgs
        {
            Id = "g6-standard-2",
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-linode/sdk/v3/go/linode"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := linode.GetInstanceType(ctx, &GetInstanceTypeArgs{
			Id: "g6-standard-2",
		}, nil)
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
import pulumi_linode as linode

default = linode.get_instance_type(id="g6-standard-2")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as linode from "@pulumi/linode";

const defaultInstanceType = pulumi.output(linode.getInstanceType({
    id: "g6-standard-2",
}));
```


{{< /example >}}





{{% /examples %}}




## Using getInstanceType {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getInstanceType<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetInstanceTypeArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetInstanceTypeResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_instance_type(</span><span class="nx">id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                      <span class="nx">label</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                      <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetInstanceTypeResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetInstanceType<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetInstanceTypeArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetInstanceTypeResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetInstanceType` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetInstanceType </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetInstanceTypeResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetInstanceTypeArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Label used to identify instance type
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="label_csharp">
<a href="#label_csharp" style="color: inherit; text-decoration: inherit;">Label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Label used to identify instance type
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="label_go">
<a href="#label_go" style="color: inherit; text-decoration: inherit;">Label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Label used to identify instance type
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="label_nodejs">
<a href="#label_nodejs" style="color: inherit; text-decoration: inherit;">label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Label used to identify instance type
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="label_python">
<a href="#label_python" style="color: inherit; text-decoration: inherit;">label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## getInstanceType Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="addons_csharp">
<a href="#addons_csharp" style="color: inherit; text-decoration: inherit;">Addons</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeaddons">Get<wbr>Instance<wbr>Type<wbr>Addons</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="class_csharp">
<a href="#class_csharp" style="color: inherit; text-decoration: inherit;">Class</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="disk_csharp">
<a href="#disk_csharp" style="color: inherit; text-decoration: inherit;">Disk</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="label_csharp">
<a href="#label_csharp" style="color: inherit; text-decoration: inherit;">Label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="memory_csharp">
<a href="#memory_csharp" style="color: inherit; text-decoration: inherit;">Memory</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="networkout_csharp">
<a href="#networkout_csharp" style="color: inherit; text-decoration: inherit;">Network<wbr>Out</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="price_csharp">
<a href="#price_csharp" style="color: inherit; text-decoration: inherit;">Price</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeprice">Get<wbr>Instance<wbr>Type<wbr>Price</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="transfer_csharp">
<a href="#transfer_csharp" style="color: inherit; text-decoration: inherit;">Transfer</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="vcpus_csharp">
<a href="#vcpus_csharp" style="color: inherit; text-decoration: inherit;">Vcpus</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="addons_go">
<a href="#addons_go" style="color: inherit; text-decoration: inherit;">Addons</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeaddons">Get<wbr>Instance<wbr>Type<wbr>Addons</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="class_go">
<a href="#class_go" style="color: inherit; text-decoration: inherit;">Class</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="disk_go">
<a href="#disk_go" style="color: inherit; text-decoration: inherit;">Disk</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="label_go">
<a href="#label_go" style="color: inherit; text-decoration: inherit;">Label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="memory_go">
<a href="#memory_go" style="color: inherit; text-decoration: inherit;">Memory</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="networkout_go">
<a href="#networkout_go" style="color: inherit; text-decoration: inherit;">Network<wbr>Out</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="price_go">
<a href="#price_go" style="color: inherit; text-decoration: inherit;">Price</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeprice">Get<wbr>Instance<wbr>Type<wbr>Price</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="transfer_go">
<a href="#transfer_go" style="color: inherit; text-decoration: inherit;">Transfer</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="vcpus_go">
<a href="#vcpus_go" style="color: inherit; text-decoration: inherit;">Vcpus</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="addons_nodejs">
<a href="#addons_nodejs" style="color: inherit; text-decoration: inherit;">addons</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeaddons">Get<wbr>Instance<wbr>Type<wbr>Addons</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="class_nodejs">
<a href="#class_nodejs" style="color: inherit; text-decoration: inherit;">class</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="disk_nodejs">
<a href="#disk_nodejs" style="color: inherit; text-decoration: inherit;">disk</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="label_nodejs">
<a href="#label_nodejs" style="color: inherit; text-decoration: inherit;">label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="memory_nodejs">
<a href="#memory_nodejs" style="color: inherit; text-decoration: inherit;">memory</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="networkout_nodejs">
<a href="#networkout_nodejs" style="color: inherit; text-decoration: inherit;">network<wbr>Out</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="price_nodejs">
<a href="#price_nodejs" style="color: inherit; text-decoration: inherit;">price</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeprice">Get<wbr>Instance<wbr>Type<wbr>Price</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="transfer_nodejs">
<a href="#transfer_nodejs" style="color: inherit; text-decoration: inherit;">transfer</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="vcpus_nodejs">
<a href="#vcpus_nodejs" style="color: inherit; text-decoration: inherit;">vcpus</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="addons_python">
<a href="#addons_python" style="color: inherit; text-decoration: inherit;">addons</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeaddons">Get<wbr>Instance<wbr>Type<wbr>Addons</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="class__python">
<a href="#class__python" style="color: inherit; text-decoration: inherit;">class_</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="disk_python">
<a href="#disk_python" style="color: inherit; text-decoration: inherit;">disk</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="label_python">
<a href="#label_python" style="color: inherit; text-decoration: inherit;">label</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="memory_python">
<a href="#memory_python" style="color: inherit; text-decoration: inherit;">memory</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="network_out_python">
<a href="#network_out_python" style="color: inherit; text-decoration: inherit;">network_<wbr>out</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="price_python">
<a href="#price_python" style="color: inherit; text-decoration: inherit;">price</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeprice">Get<wbr>Instance<wbr>Type<wbr>Price</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="transfer_python">
<a href="#transfer_python" style="color: inherit; text-decoration: inherit;">transfer</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="vcpus_python">
<a href="#vcpus_python" style="color: inherit; text-decoration: inherit;">vcpus</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getinstancetypeaddons">Get<wbr>Instance<wbr>Type<wbr>Addons</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="backups_csharp">
<a href="#backups_csharp" style="color: inherit; text-decoration: inherit;">Backups</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeaddonsbackups">Get<wbr>Instance<wbr>Type<wbr>Addons<wbr>Backups</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="backups_go">
<a href="#backups_go" style="color: inherit; text-decoration: inherit;">Backups</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeaddonsbackups">Get<wbr>Instance<wbr>Type<wbr>Addons<wbr>Backups</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="backups_nodejs">
<a href="#backups_nodejs" style="color: inherit; text-decoration: inherit;">backups</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeaddonsbackups">Get<wbr>Instance<wbr>Type<wbr>Addons<wbr>Backups</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="backups_python">
<a href="#backups_python" style="color: inherit; text-decoration: inherit;">backups</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeaddonsbackups">Get<wbr>Instance<wbr>Type<wbr>Addons<wbr>Backups</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="getinstancetypeaddonsbackups">Get<wbr>Instance<wbr>Type<wbr>Addons<wbr>Backups</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="price_csharp">
<a href="#price_csharp" style="color: inherit; text-decoration: inherit;">Price</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeaddonsbackupsprice">Get<wbr>Instance<wbr>Type<wbr>Addons<wbr>Backups<wbr>Price</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="price_go">
<a href="#price_go" style="color: inherit; text-decoration: inherit;">Price</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeaddonsbackupsprice">Get<wbr>Instance<wbr>Type<wbr>Addons<wbr>Backups<wbr>Price</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="price_nodejs">
<a href="#price_nodejs" style="color: inherit; text-decoration: inherit;">price</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeaddonsbackupsprice">Get<wbr>Instance<wbr>Type<wbr>Addons<wbr>Backups<wbr>Price</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="price_python">
<a href="#price_python" style="color: inherit; text-decoration: inherit;">price</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getinstancetypeaddonsbackupsprice">Get<wbr>Instance<wbr>Type<wbr>Addons<wbr>Backups<wbr>Price</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="getinstancetypeaddonsbackupsprice">Get<wbr>Instance<wbr>Type<wbr>Addons<wbr>Backups<wbr>Price</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="hourly_csharp">
<a href="#hourly_csharp" style="color: inherit; text-decoration: inherit;">Hourly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">double</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="monthly_csharp">
<a href="#monthly_csharp" style="color: inherit; text-decoration: inherit;">Monthly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">double</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="hourly_go">
<a href="#hourly_go" style="color: inherit; text-decoration: inherit;">Hourly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">float64</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="monthly_go">
<a href="#monthly_go" style="color: inherit; text-decoration: inherit;">Monthly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">float64</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="hourly_nodejs">
<a href="#hourly_nodejs" style="color: inherit; text-decoration: inherit;">hourly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="monthly_nodejs">
<a href="#monthly_nodejs" style="color: inherit; text-decoration: inherit;">monthly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="hourly_python">
<a href="#hourly_python" style="color: inherit; text-decoration: inherit;">hourly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="monthly_python">
<a href="#monthly_python" style="color: inherit; text-decoration: inherit;">monthly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="getinstancetypeprice">Get<wbr>Instance<wbr>Type<wbr>Price</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="hourly_csharp">
<a href="#hourly_csharp" style="color: inherit; text-decoration: inherit;">Hourly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">double</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="monthly_csharp">
<a href="#monthly_csharp" style="color: inherit; text-decoration: inherit;">Monthly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">double</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="hourly_go">
<a href="#hourly_go" style="color: inherit; text-decoration: inherit;">Hourly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">float64</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="monthly_go">
<a href="#monthly_go" style="color: inherit; text-decoration: inherit;">Monthly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">float64</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="hourly_nodejs">
<a href="#hourly_nodejs" style="color: inherit; text-decoration: inherit;">hourly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="monthly_nodejs">
<a href="#monthly_nodejs" style="color: inherit; text-decoration: inherit;">monthly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="hourly_python">
<a href="#hourly_python" style="color: inherit; text-decoration: inherit;">hourly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="monthly_python">
<a href="#monthly_python" style="color: inherit; text-decoration: inherit;">monthly</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-linode">https://github.com/pulumi/pulumi-linode</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`linode` Terraform Provider](https://github.com/linode/terraform-provider-linode).{{% /md %}}</dd>
</dl>
