
---
title: "getDomains"
title_tag: "digitalocean.getDomains"
meta_desc: "Documentation for the digitalocean.getDomains function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Get information on domains for use in other resources, with the ability to filter and sort the results.
If no filters are specified, all domains will be returned.

This data source is useful if the domains in question are not managed by this provider or you need to
utilize any of the domains' data.

Note: You can use the `digitalocean.Domain` data source to obtain metadata
about a single domain if you already know the `name`.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using DigitalOcean = Pulumi.DigitalOcean;

class MyStack : Stack
{
    public MyStack()
    {
        var examples = Output.Create(DigitalOcean.GetDomains.InvokeAsync(new DigitalOcean.GetDomainsArgs
        {
            Filters = 
            {
                new DigitalOcean.Inputs.GetDomainsFilterArgs
                {
                    Key = "name",
                    MatchBy = "re",
                    Values = 
                    {
                        "example\\.com$",
                    },
                },
            },
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"fmt"

	"github.com/pulumi/pulumi-digitalocean/sdk/v4/go/digitalocean"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := digitalocean.GetDomains(ctx, &digitalocean.GetDomainsArgs{
			Filters: []digitalocean.GetDomainsFilter{
				digitalocean.GetDomainsFilter{
					Key:     "name",
					MatchBy: "re",
					Values: []string{
						fmt.Sprintf("%v%v", "example\\.com", "$"),
					},
				},
			},
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
import pulumi_digitalocean as digitalocean

examples = digitalocean.get_domains(filters=[digitalocean.GetDomainsFilterArgs(
    key="name",
    match_by="re",
    values=["example\\.com$"],
)])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as digitalocean from "@pulumi/digitalocean";

const examples = pulumi.output(digitalocean.getDomains({
    filters: [{
        key: "name",
        matchBy: "re",
        values: ["example\\.com$"],
    }],
}));
```


{{< /example >}}





{{% /examples %}}




## Using getDomains {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getDomains<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetDomainsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetDomainsResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_domains(</span><span class="nx">filters</span><span class="p">:</span> <span class="nx">Optional[Sequence[GetDomainsFilter]]</span> = None<span class="p">,</span>
                <span class="nx">sorts</span><span class="p">:</span> <span class="nx">Optional[Sequence[GetDomainsSort]]</span> = None<span class="p">,</span>
                <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetDomainsResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetDomains<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetDomainsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetDomainsResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetDomains` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetDomains </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetDomainsResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetDomainsArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="filters_csharp">
<a href="#filters_csharp" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainsfilter">List&lt;Pulumi.<wbr>Digital<wbr>Ocean.<wbr>Inputs.<wbr>Get<wbr>Domains<wbr>Filter&gt;</a></span>
    </dt>
    <dd>{{% md %}}Filter the results.
The `filter` block is documented below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="sorts_csharp">
<a href="#sorts_csharp" style="color: inherit; text-decoration: inherit;">Sorts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainssort">List&lt;Pulumi.<wbr>Digital<wbr>Ocean.<wbr>Inputs.<wbr>Get<wbr>Domains<wbr>Sort&gt;</a></span>
    </dt>
    <dd>{{% md %}}Sort the results.
The `sort` block is documented below.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="filters_go">
<a href="#filters_go" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainsfilter">[]Get<wbr>Domains<wbr>Filter</a></span>
    </dt>
    <dd>{{% md %}}Filter the results.
The `filter` block is documented below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="sorts_go">
<a href="#sorts_go" style="color: inherit; text-decoration: inherit;">Sorts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainssort">[]Get<wbr>Domains<wbr>Sort</a></span>
    </dt>
    <dd>{{% md %}}Sort the results.
The `sort` block is documented below.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="filters_nodejs">
<a href="#filters_nodejs" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainsfilter">Get<wbr>Domains<wbr>Filter[]</a></span>
    </dt>
    <dd>{{% md %}}Filter the results.
The `filter` block is documented below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="sorts_nodejs">
<a href="#sorts_nodejs" style="color: inherit; text-decoration: inherit;">sorts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainssort">Get<wbr>Domains<wbr>Sort[]</a></span>
    </dt>
    <dd>{{% md %}}Sort the results.
The `sort` block is documented below.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="filters_python">
<a href="#filters_python" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainsfilter">Sequence[Get<wbr>Domains<wbr>Filter]</a></span>
    </dt>
    <dd>{{% md %}}Filter the results.
The `filter` block is documented below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="sorts_python">
<a href="#sorts_python" style="color: inherit; text-decoration: inherit;">sorts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainssort">Sequence[Get<wbr>Domains<wbr>Sort]</a></span>
    </dt>
    <dd>{{% md %}}Sort the results.
The `sort` block is documented below.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getDomains Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="domains_csharp">
<a href="#domains_csharp" style="color: inherit; text-decoration: inherit;">Domains</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainsdomain">List&lt;Pulumi.<wbr>Digital<wbr>Ocean.<wbr>Outputs.<wbr>Get<wbr>Domains<wbr>Domain&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of domains satisfying any `filter` and `sort` criteria. Each domain has the following attributes:
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
        <span id="filters_csharp">
<a href="#filters_csharp" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainsfilter">List&lt;Pulumi.<wbr>Digital<wbr>Ocean.<wbr>Outputs.<wbr>Get<wbr>Domains<wbr>Filter&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sorts_csharp">
<a href="#sorts_csharp" style="color: inherit; text-decoration: inherit;">Sorts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainssort">List&lt;Pulumi.<wbr>Digital<wbr>Ocean.<wbr>Outputs.<wbr>Get<wbr>Domains<wbr>Sort&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="domains_go">
<a href="#domains_go" style="color: inherit; text-decoration: inherit;">Domains</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainsdomain">[]Get<wbr>Domains<wbr>Domain</a></span>
    </dt>
    <dd>{{% md %}}A list of domains satisfying any `filter` and `sort` criteria. Each domain has the following attributes:
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
        <span id="filters_go">
<a href="#filters_go" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainsfilter">[]Get<wbr>Domains<wbr>Filter</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sorts_go">
<a href="#sorts_go" style="color: inherit; text-decoration: inherit;">Sorts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainssort">[]Get<wbr>Domains<wbr>Sort</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="domains_nodejs">
<a href="#domains_nodejs" style="color: inherit; text-decoration: inherit;">domains</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainsdomain">Get<wbr>Domains<wbr>Domain[]</a></span>
    </dt>
    <dd>{{% md %}}A list of domains satisfying any `filter` and `sort` criteria. Each domain has the following attributes:
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
        <span id="filters_nodejs">
<a href="#filters_nodejs" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainsfilter">Get<wbr>Domains<wbr>Filter[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sorts_nodejs">
<a href="#sorts_nodejs" style="color: inherit; text-decoration: inherit;">sorts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainssort">Get<wbr>Domains<wbr>Sort[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="domains_python">
<a href="#domains_python" style="color: inherit; text-decoration: inherit;">domains</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainsdomain">Sequence[Get<wbr>Domains<wbr>Domain]</a></span>
    </dt>
    <dd>{{% md %}}A list of domains satisfying any `filter` and `sort` criteria. Each domain has the following attributes:
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
        <span id="filters_python">
<a href="#filters_python" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainsfilter">Sequence[Get<wbr>Domains<wbr>Filter]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sorts_python">
<a href="#sorts_python" style="color: inherit; text-decoration: inherit;">sorts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdomainssort">Sequence[Get<wbr>Domains<wbr>Sort]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getdomainsdomain">Get<wbr>Domains<wbr>Domain</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Required) The name of the domain.
- `ttl`-  The TTL of the domain.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="ttl_csharp">
<a href="#ttl_csharp" style="color: inherit; text-decoration: inherit;">Ttl</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="urn_csharp">
<a href="#urn_csharp" style="color: inherit; text-decoration: inherit;">Urn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The uniform resource name of the domain
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Required) The name of the domain.
- `ttl`-  The TTL of the domain.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="ttl_go">
<a href="#ttl_go" style="color: inherit; text-decoration: inherit;">Ttl</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="urn_go">
<a href="#urn_go" style="color: inherit; text-decoration: inherit;">Urn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The uniform resource name of the domain
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Required) The name of the domain.
- `ttl`-  The TTL of the domain.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="ttl_nodejs">
<a href="#ttl_nodejs" style="color: inherit; text-decoration: inherit;">ttl</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="urn_nodejs">
<a href="#urn_nodejs" style="color: inherit; text-decoration: inherit;">urn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The uniform resource name of the domain
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Required) The name of the domain.
- `ttl`-  The TTL of the domain.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="ttl_python">
<a href="#ttl_python" style="color: inherit; text-decoration: inherit;">ttl</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="urn_python">
<a href="#urn_python" style="color: inherit; text-decoration: inherit;">urn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The uniform resource name of the domain
{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="getdomainsfilter">Get<wbr>Domains<wbr>Filter</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_csharp">
<a href="#key_csharp" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Filter the domains by this key. This may be one of `name`, `urn`, and `ttl`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_csharp">
<a href="#values_csharp" style="color: inherit; text-decoration: inherit;">Values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of values to match against the `key` field. Only retrieves domains
where the `key` field takes on one or more of the values provided here.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="all_csharp">
<a href="#all_csharp" style="color: inherit; text-decoration: inherit;">All</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Set to `true` to require that a field match all of the `values` instead of just one or more of
them. This is useful when matching against multi-valued fields such as lists or sets where you want to ensure
that all of the `values` are present in the list or set.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="matchby_csharp">
<a href="#matchby_csharp" style="color: inherit; text-decoration: inherit;">Match<wbr>By</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}One of `exact` (default), `re`, or `substring`. For string-typed fields, specify `re` to
match by using the `values` as regular expressions, or specify `substring` to match by treating the `values` as
substrings to find within the string field.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_go">
<a href="#key_go" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Filter the domains by this key. This may be one of `name`, `urn`, and `ttl`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_go">
<a href="#values_go" style="color: inherit; text-decoration: inherit;">Values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of values to match against the `key` field. Only retrieves domains
where the `key` field takes on one or more of the values provided here.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="all_go">
<a href="#all_go" style="color: inherit; text-decoration: inherit;">All</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Set to `true` to require that a field match all of the `values` instead of just one or more of
them. This is useful when matching against multi-valued fields such as lists or sets where you want to ensure
that all of the `values` are present in the list or set.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="matchby_go">
<a href="#matchby_go" style="color: inherit; text-decoration: inherit;">Match<wbr>By</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}One of `exact` (default), `re`, or `substring`. For string-typed fields, specify `re` to
match by using the `values` as regular expressions, or specify `substring` to match by treating the `values` as
substrings to find within the string field.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_nodejs">
<a href="#key_nodejs" style="color: inherit; text-decoration: inherit;">key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Filter the domains by this key. This may be one of `name`, `urn`, and `ttl`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_nodejs">
<a href="#values_nodejs" style="color: inherit; text-decoration: inherit;">values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of values to match against the `key` field. Only retrieves domains
where the `key` field takes on one or more of the values provided here.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="all_nodejs">
<a href="#all_nodejs" style="color: inherit; text-decoration: inherit;">all</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Set to `true` to require that a field match all of the `values` instead of just one or more of
them. This is useful when matching against multi-valued fields such as lists or sets where you want to ensure
that all of the `values` are present in the list or set.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="matchby_nodejs">
<a href="#matchby_nodejs" style="color: inherit; text-decoration: inherit;">match<wbr>By</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}One of `exact` (default), `re`, or `substring`. For string-typed fields, specify `re` to
match by using the `values` as regular expressions, or specify `substring` to match by treating the `values` as
substrings to find within the string field.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_python">
<a href="#key_python" style="color: inherit; text-decoration: inherit;">key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Filter the domains by this key. This may be one of `name`, `urn`, and `ttl`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_python">
<a href="#values_python" style="color: inherit; text-decoration: inherit;">values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of values to match against the `key` field. Only retrieves domains
where the `key` field takes on one or more of the values provided here.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="all_python">
<a href="#all_python" style="color: inherit; text-decoration: inherit;">all</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Set to `true` to require that a field match all of the `values` instead of just one or more of
them. This is useful when matching against multi-valued fields such as lists or sets where you want to ensure
that all of the `values` are present in the list or set.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="match_by_python">
<a href="#match_by_python" style="color: inherit; text-decoration: inherit;">match_<wbr>by</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}One of `exact` (default), `re`, or `substring`. For string-typed fields, specify `re` to
match by using the `values` as regular expressions, or specify `substring` to match by treating the `values` as
substrings to find within the string field.
{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="getdomainssort">Get<wbr>Domains<wbr>Sort</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_csharp">
<a href="#key_csharp" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Sort the domains by this key. This may be one of `name`, `urn`, and `ttl`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="direction_csharp">
<a href="#direction_csharp" style="color: inherit; text-decoration: inherit;">Direction</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The sort direction. This may be either `asc` or `desc`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_go">
<a href="#key_go" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Sort the domains by this key. This may be one of `name`, `urn`, and `ttl`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="direction_go">
<a href="#direction_go" style="color: inherit; text-decoration: inherit;">Direction</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The sort direction. This may be either `asc` or `desc`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_nodejs">
<a href="#key_nodejs" style="color: inherit; text-decoration: inherit;">key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Sort the domains by this key. This may be one of `name`, `urn`, and `ttl`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="direction_nodejs">
<a href="#direction_nodejs" style="color: inherit; text-decoration: inherit;">direction</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The sort direction. This may be either `asc` or `desc`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_python">
<a href="#key_python" style="color: inherit; text-decoration: inherit;">key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Sort the domains by this key. This may be one of `name`, `urn`, and `ttl`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="direction_python">
<a href="#direction_python" style="color: inherit; text-decoration: inherit;">direction</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The sort direction. This may be either `asc` or `desc`.
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-digitalocean">https://github.com/pulumi/pulumi-digitalocean</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`digitalocean` Terraform Provider](https://github.com/digitalocean/terraform-provider-digitalocean).{{% /md %}}</dd>
</dl>
