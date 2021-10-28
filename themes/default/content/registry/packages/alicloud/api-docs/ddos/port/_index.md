
---
title: "Port"
title_tag: "alicloud.ddos.Port"
meta_desc: "Documentation for the alicloud.ddos.Port resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Provides a Anti-DDoS Pro Port resource.

For information about Anti-DDoS Pro Port and how to use it, see [What is Port](https://www.alibabacloud.com/help/en/doc-detail/157482.htm).

> **NOTE:** Available in v1.123.0+.

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
        var exampleDdosCooInstance = new AliCloud.Ddos.DdosCooInstance("exampleDdosCooInstance", new AliCloud.Ddos.DdosCooInstanceArgs
        {
            Bandwidth = "30",
            BaseBandwidth = "30",
            ServiceBandwidth = "100",
            PortCount = "50",
            DomainCount = "50",
        });
        var examplePort = new AliCloud.Ddos.Port("examplePort", new AliCloud.Ddos.PortArgs
        {
            InstanceId = exampleDdosCooInstance.Id,
            FrontendPort = "7001",
            FrontendProtocol = "tcp",
            RealServers = 
            {
                "1.1.1.1",
                "2.2.2.2",
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
	"github.com/pulumi/pulumi-alicloud/sdk/v3/go/alicloud/ddos"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		exampleDdosCooInstance, err := ddos.NewDdosCooInstance(ctx, "exampleDdosCooInstance", &ddos.DdosCooInstanceArgs{
			Bandwidth:        pulumi.String("30"),
			BaseBandwidth:    pulumi.String("30"),
			ServiceBandwidth: pulumi.String("100"),
			PortCount:        pulumi.String("50"),
			DomainCount:      pulumi.String("50"),
		})
		if err != nil {
			return err
		}
		_, err = ddos.NewPort(ctx, "examplePort", &ddos.PortArgs{
			InstanceId:       exampleDdosCooInstance.ID(),
			FrontendPort:     pulumi.String("7001"),
			FrontendProtocol: pulumi.String("tcp"),
			RealServers: pulumi.StringArray{
				pulumi.String("1.1.1.1"),
				pulumi.String("2.2.2.2"),
			},
		})
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
import pulumi_alicloud as alicloud

example_ddos_coo_instance = alicloud.ddos.DdosCooInstance("exampleDdosCooInstance",
    bandwidth="30",
    base_bandwidth="30",
    service_bandwidth="100",
    port_count="50",
    domain_count="50")
example_port = alicloud.ddos.Port("examplePort",
    instance_id=example_ddos_coo_instance.id,
    frontend_port="7001",
    frontend_protocol="tcp",
    real_servers=[
        "1.1.1.1",
        "2.2.2.2",
    ])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

const exampleDdosCooInstance = new alicloud.ddos.DdosCooInstance("exampleDdosCooInstance", {
    bandwidth: "30",
    baseBandwidth: "30",
    serviceBandwidth: "100",
    portCount: "50",
    domainCount: "50",
});
const examplePort = new alicloud.ddos.Port("examplePort", {
    instanceId: exampleDdosCooInstance.id,
    frontendPort: "7001",
    frontendProtocol: "tcp",
    realServers: [
        "1.1.1.1",
        "2.2.2.2",
    ],
});
```


{{< /example >}}





{{% /examples %}}




## Create a Port Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">Port</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">PortArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Port</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
         <span class="nx">backend_port</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
         <span class="nx">frontend_port</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
         <span class="nx">frontend_protocol</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
         <span class="nx">instance_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
         <span class="nx">real_servers</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Port</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
         <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">PortArgs</a></span><span class="p">,</span>
         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewPort</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">PortArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Port</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">Port</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">PortArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">PortArgs</a></span>
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
        <span class="property-type"><a href="#inputs">PortArgs</a></span>
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
        <span class="property-type"><a href="#inputs">PortArgs</a></span>
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
        <span class="property-type"><a href="#inputs">PortArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## Port Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The Port resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="frontendport_csharp">
<a href="#frontendport_csharp" style="color: inherit; text-decoration: inherit;">Frontend<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The forwarding port.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="frontendprotocol_csharp">
<a href="#frontendprotocol_csharp" style="color: inherit; text-decoration: inherit;">Frontend<wbr>Protocol</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The forwarding protocol. Valid values `tcp` and `udp`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="instanceid_csharp">
<a href="#instanceid_csharp" style="color: inherit; text-decoration: inherit;">Instance<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of Ddoscoo instance.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="realservers_csharp">
<a href="#realservers_csharp" style="color: inherit; text-decoration: inherit;">Real<wbr>Servers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}List of source IP addresses.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="backendport_csharp">
<a href="#backendport_csharp" style="color: inherit; text-decoration: inherit;">Backend<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The port of the origin server.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="frontendport_go">
<a href="#frontendport_go" style="color: inherit; text-decoration: inherit;">Frontend<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The forwarding port.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="frontendprotocol_go">
<a href="#frontendprotocol_go" style="color: inherit; text-decoration: inherit;">Frontend<wbr>Protocol</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The forwarding protocol. Valid values `tcp` and `udp`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="instanceid_go">
<a href="#instanceid_go" style="color: inherit; text-decoration: inherit;">Instance<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of Ddoscoo instance.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="realservers_go">
<a href="#realservers_go" style="color: inherit; text-decoration: inherit;">Real<wbr>Servers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of source IP addresses.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="backendport_go">
<a href="#backendport_go" style="color: inherit; text-decoration: inherit;">Backend<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The port of the origin server.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="frontendport_nodejs">
<a href="#frontendport_nodejs" style="color: inherit; text-decoration: inherit;">frontend<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The forwarding port.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="frontendprotocol_nodejs">
<a href="#frontendprotocol_nodejs" style="color: inherit; text-decoration: inherit;">frontend<wbr>Protocol</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The forwarding protocol. Valid values `tcp` and `udp`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="instanceid_nodejs">
<a href="#instanceid_nodejs" style="color: inherit; text-decoration: inherit;">instance<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of Ddoscoo instance.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="realservers_nodejs">
<a href="#realservers_nodejs" style="color: inherit; text-decoration: inherit;">real<wbr>Servers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}List of source IP addresses.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="backendport_nodejs">
<a href="#backendport_nodejs" style="color: inherit; text-decoration: inherit;">backend<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The port of the origin server.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="frontend_port_python">
<a href="#frontend_port_python" style="color: inherit; text-decoration: inherit;">frontend_<wbr>port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The forwarding port.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="frontend_protocol_python">
<a href="#frontend_protocol_python" style="color: inherit; text-decoration: inherit;">frontend_<wbr>protocol</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The forwarding protocol. Valid values `tcp` and `udp`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="instance_id_python">
<a href="#instance_id_python" style="color: inherit; text-decoration: inherit;">instance_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of Ddoscoo instance.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="real_servers_python">
<a href="#real_servers_python" style="color: inherit; text-decoration: inherit;">real_<wbr>servers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}List of source IP addresses.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="backend_port_python">
<a href="#backend_port_python" style="color: inherit; text-decoration: inherit;">backend_<wbr>port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The port of the origin server.
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the Port resource produces the following output properties:



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



## Look up an Existing Port Resource {#look-up}

Get an existing Port resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">PortState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">Port</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">backend_port</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">frontend_port</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">frontend_protocol</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">instance_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">real_servers</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">) -&gt;</span> Port</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetPort<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">PortState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Port</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">Port</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">PortState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span id="state_backendport_csharp">
<a href="#state_backendport_csharp" style="color: inherit; text-decoration: inherit;">Backend<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The port of the origin server.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_frontendport_csharp">
<a href="#state_frontendport_csharp" style="color: inherit; text-decoration: inherit;">Frontend<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The forwarding port.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_frontendprotocol_csharp">
<a href="#state_frontendprotocol_csharp" style="color: inherit; text-decoration: inherit;">Frontend<wbr>Protocol</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The forwarding protocol. Valid values `tcp` and `udp`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_instanceid_csharp">
<a href="#state_instanceid_csharp" style="color: inherit; text-decoration: inherit;">Instance<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of Ddoscoo instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_realservers_csharp">
<a href="#state_realservers_csharp" style="color: inherit; text-decoration: inherit;">Real<wbr>Servers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}List of source IP addresses.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_backendport_go">
<a href="#state_backendport_go" style="color: inherit; text-decoration: inherit;">Backend<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The port of the origin server.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_frontendport_go">
<a href="#state_frontendport_go" style="color: inherit; text-decoration: inherit;">Frontend<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The forwarding port.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_frontendprotocol_go">
<a href="#state_frontendprotocol_go" style="color: inherit; text-decoration: inherit;">Frontend<wbr>Protocol</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The forwarding protocol. Valid values `tcp` and `udp`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_instanceid_go">
<a href="#state_instanceid_go" style="color: inherit; text-decoration: inherit;">Instance<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of Ddoscoo instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_realservers_go">
<a href="#state_realservers_go" style="color: inherit; text-decoration: inherit;">Real<wbr>Servers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of source IP addresses.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_backendport_nodejs">
<a href="#state_backendport_nodejs" style="color: inherit; text-decoration: inherit;">backend<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The port of the origin server.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_frontendport_nodejs">
<a href="#state_frontendport_nodejs" style="color: inherit; text-decoration: inherit;">frontend<wbr>Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The forwarding port.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_frontendprotocol_nodejs">
<a href="#state_frontendprotocol_nodejs" style="color: inherit; text-decoration: inherit;">frontend<wbr>Protocol</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The forwarding protocol. Valid values `tcp` and `udp`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_instanceid_nodejs">
<a href="#state_instanceid_nodejs" style="color: inherit; text-decoration: inherit;">instance<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of Ddoscoo instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_realservers_nodejs">
<a href="#state_realservers_nodejs" style="color: inherit; text-decoration: inherit;">real<wbr>Servers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}List of source IP addresses.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_backend_port_python">
<a href="#state_backend_port_python" style="color: inherit; text-decoration: inherit;">backend_<wbr>port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The port of the origin server.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_frontend_port_python">
<a href="#state_frontend_port_python" style="color: inherit; text-decoration: inherit;">frontend_<wbr>port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The forwarding port.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_frontend_protocol_python">
<a href="#state_frontend_protocol_python" style="color: inherit; text-decoration: inherit;">frontend_<wbr>protocol</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The forwarding protocol. Valid values `tcp` and `udp`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_instance_id_python">
<a href="#state_instance_id_python" style="color: inherit; text-decoration: inherit;">instance_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of Ddoscoo instance.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_real_servers_python">
<a href="#state_real_servers_python" style="color: inherit; text-decoration: inherit;">real_<wbr>servers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}List of source IP addresses.
{{% /md %}}</dd></dl>
{{% /choosable %}}





## Import


Anti-DDoS Pro Port can be imported using the id, e.g.

```sh
 $ pulumi import alicloud:ddos/port:Port example <instance_id>:<frontend_port>:<frontend_protocol>
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-alicloud">https://github.com/pulumi/pulumi-alicloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`alicloud` Terraform Provider](https://github.com/aliyun/terraform-provider-alicloud).{{% /md %}}</dd>
</dl>
