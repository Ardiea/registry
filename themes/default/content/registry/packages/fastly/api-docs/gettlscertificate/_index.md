
---
title: "getTlsCertificate"
title_tag: "fastly.getTlsCertificate"
meta_desc: "Documentation for the fastly.getTlsCertificate function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to get information of a TLS certificate for use with other resources.

> **Warning:** The data source's filters are applied using an **AND** boolean operator, so depending on the combination
of filters, they may become mutually exclusive. The exception to this is `id` which must not be specified in combination
with any of the others.

> **Note:** If more or less than a single match is returned by the search, this provider will fail. Ensure that your search is specific enough to return a single key.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Fastly = Pulumi.Fastly;

class MyStack : Stack
{
    public MyStack()
    {
        var example = Output.Create(Fastly.GetTlsCertificate.InvokeAsync(new Fastly.GetTlsCertificateArgs
        {
            Name = "example.com",
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-fastly/sdk/v3/go/fastly"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "example.com"
		_, err := fastly.LookupTlsCertificate(ctx, &fastly.LookupTlsCertificateArgs{
			Name: &opt0,
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
import pulumi_fastly as fastly

example = fastly.get_tls_certificate(name="example.com")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as fastly from "@pulumi/fastly";

const example = pulumi.output(fastly.getTlsCertificate({
    name: "example.com",
}));
```


{{< /example >}}





{{% /examples %}}




## Using getTlsCertificate {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getTlsCertificate<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetTlsCertificateArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetTlsCertificateResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_tls_certificate(</span><span class="nx">domains</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
                        <span class="nx">id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">issued_to</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">issuer</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetTlsCertificateResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupTlsCertificate<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupTlsCertificateArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupTlsCertificateResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupTlsCertificate` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetTlsCertificate </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetTlsCertificateResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetTlsCertificateArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="domains_csharp">
<a href="#domains_csharp" style="color: inherit; text-decoration: inherit;">Domains</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Domains that are listed in any certificates' Subject Alternative Names (SAN) list.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Unique ID assigned to certificate by Fastly
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="issuedto_csharp">
<a href="#issuedto_csharp" style="color: inherit; text-decoration: inherit;">Issued<wbr>To</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The hostname for which a certificate was issued.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="issuer_csharp">
<a href="#issuer_csharp" style="color: inherit; text-decoration: inherit;">Issuer</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The certificate authority that issued the certificate.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human-readable name used to identify the certificate. Defaults to the certificate's Common Name or first Subject Alternative Name entry.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="domains_go">
<a href="#domains_go" style="color: inherit; text-decoration: inherit;">Domains</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Domains that are listed in any certificates' Subject Alternative Names (SAN) list.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Unique ID assigned to certificate by Fastly
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="issuedto_go">
<a href="#issuedto_go" style="color: inherit; text-decoration: inherit;">Issued<wbr>To</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The hostname for which a certificate was issued.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="issuer_go">
<a href="#issuer_go" style="color: inherit; text-decoration: inherit;">Issuer</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The certificate authority that issued the certificate.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human-readable name used to identify the certificate. Defaults to the certificate's Common Name or first Subject Alternative Name entry.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="domains_nodejs">
<a href="#domains_nodejs" style="color: inherit; text-decoration: inherit;">domains</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Domains that are listed in any certificates' Subject Alternative Names (SAN) list.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Unique ID assigned to certificate by Fastly
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="issuedto_nodejs">
<a href="#issuedto_nodejs" style="color: inherit; text-decoration: inherit;">issued<wbr>To</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The hostname for which a certificate was issued.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="issuer_nodejs">
<a href="#issuer_nodejs" style="color: inherit; text-decoration: inherit;">issuer</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The certificate authority that issued the certificate.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human-readable name used to identify the certificate. Defaults to the certificate's Common Name or first Subject Alternative Name entry.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="domains_python">
<a href="#domains_python" style="color: inherit; text-decoration: inherit;">domains</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Domains that are listed in any certificates' Subject Alternative Names (SAN) list.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Unique ID assigned to certificate by Fastly
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="issued_to_python">
<a href="#issued_to_python" style="color: inherit; text-decoration: inherit;">issued_<wbr>to</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The hostname for which a certificate was issued.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="issuer_python">
<a href="#issuer_python" style="color: inherit; text-decoration: inherit;">issuer</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The certificate authority that issued the certificate.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Human-readable name used to identify the certificate. Defaults to the certificate's Common Name or first Subject Alternative Name entry.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getTlsCertificate Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_csharp">
<a href="#createdat_csharp" style="color: inherit; text-decoration: inherit;">Created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the certificate was created
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="domains_csharp">
<a href="#domains_csharp" style="color: inherit; text-decoration: inherit;">Domains</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Domains that are listed in any certificates' Subject Alternative Names (SAN) list.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Unique ID assigned to certificate by Fastly
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="issuedto_csharp">
<a href="#issuedto_csharp" style="color: inherit; text-decoration: inherit;">Issued<wbr>To</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The hostname for which a certificate was issued.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="issuer_csharp">
<a href="#issuer_csharp" style="color: inherit; text-decoration: inherit;">Issuer</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The certificate authority that issued the certificate.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human-readable name used to identify the certificate. Defaults to the certificate's Common Name or first Subject Alternative Name entry.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="replace_csharp">
<a href="#replace_csharp" style="color: inherit; text-decoration: inherit;">Replace</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}A recommendation from Fastly indicating the key associated with this certificate is in need of rotation
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="serialnumber_csharp">
<a href="#serialnumber_csharp" style="color: inherit; text-decoration: inherit;">Serial<wbr>Number</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A value assigned by the issuer that is unique to a certificate
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="signaturealgorithm_csharp">
<a href="#signaturealgorithm_csharp" style="color: inherit; text-decoration: inherit;">Signature<wbr>Algorithm</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The algorithm used to sign the certificate
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updatedat_csharp">
<a href="#updatedat_csharp" style="color: inherit; text-decoration: inherit;">Updated<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the certificate was last updated
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_go">
<a href="#createdat_go" style="color: inherit; text-decoration: inherit;">Created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the certificate was created
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="domains_go">
<a href="#domains_go" style="color: inherit; text-decoration: inherit;">Domains</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Domains that are listed in any certificates' Subject Alternative Names (SAN) list.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Unique ID assigned to certificate by Fastly
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="issuedto_go">
<a href="#issuedto_go" style="color: inherit; text-decoration: inherit;">Issued<wbr>To</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The hostname for which a certificate was issued.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="issuer_go">
<a href="#issuer_go" style="color: inherit; text-decoration: inherit;">Issuer</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The certificate authority that issued the certificate.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human-readable name used to identify the certificate. Defaults to the certificate's Common Name or first Subject Alternative Name entry.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="replace_go">
<a href="#replace_go" style="color: inherit; text-decoration: inherit;">Replace</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}A recommendation from Fastly indicating the key associated with this certificate is in need of rotation
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="serialnumber_go">
<a href="#serialnumber_go" style="color: inherit; text-decoration: inherit;">Serial<wbr>Number</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A value assigned by the issuer that is unique to a certificate
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="signaturealgorithm_go">
<a href="#signaturealgorithm_go" style="color: inherit; text-decoration: inherit;">Signature<wbr>Algorithm</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The algorithm used to sign the certificate
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updatedat_go">
<a href="#updatedat_go" style="color: inherit; text-decoration: inherit;">Updated<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the certificate was last updated
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_nodejs">
<a href="#createdat_nodejs" style="color: inherit; text-decoration: inherit;">created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the certificate was created
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="domains_nodejs">
<a href="#domains_nodejs" style="color: inherit; text-decoration: inherit;">domains</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Domains that are listed in any certificates' Subject Alternative Names (SAN) list.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Unique ID assigned to certificate by Fastly
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="issuedto_nodejs">
<a href="#issuedto_nodejs" style="color: inherit; text-decoration: inherit;">issued<wbr>To</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The hostname for which a certificate was issued.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="issuer_nodejs">
<a href="#issuer_nodejs" style="color: inherit; text-decoration: inherit;">issuer</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The certificate authority that issued the certificate.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human-readable name used to identify the certificate. Defaults to the certificate's Common Name or first Subject Alternative Name entry.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="replace_nodejs">
<a href="#replace_nodejs" style="color: inherit; text-decoration: inherit;">replace</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}A recommendation from Fastly indicating the key associated with this certificate is in need of rotation
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="serialnumber_nodejs">
<a href="#serialnumber_nodejs" style="color: inherit; text-decoration: inherit;">serial<wbr>Number</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A value assigned by the issuer that is unique to a certificate
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="signaturealgorithm_nodejs">
<a href="#signaturealgorithm_nodejs" style="color: inherit; text-decoration: inherit;">signature<wbr>Algorithm</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The algorithm used to sign the certificate
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updatedat_nodejs">
<a href="#updatedat_nodejs" style="color: inherit; text-decoration: inherit;">updated<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the certificate was last updated
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="created_at_python">
<a href="#created_at_python" style="color: inherit; text-decoration: inherit;">created_<wbr>at</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the certificate was created
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="domains_python">
<a href="#domains_python" style="color: inherit; text-decoration: inherit;">domains</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Domains that are listed in any certificates' Subject Alternative Names (SAN) list.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Unique ID assigned to certificate by Fastly
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="issued_to_python">
<a href="#issued_to_python" style="color: inherit; text-decoration: inherit;">issued_<wbr>to</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The hostname for which a certificate was issued.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="issuer_python">
<a href="#issuer_python" style="color: inherit; text-decoration: inherit;">issuer</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The certificate authority that issued the certificate.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Human-readable name used to identify the certificate. Defaults to the certificate's Common Name or first Subject Alternative Name entry.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="replace_python">
<a href="#replace_python" style="color: inherit; text-decoration: inherit;">replace</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}A recommendation from Fastly indicating the key associated with this certificate is in need of rotation
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="serial_number_python">
<a href="#serial_number_python" style="color: inherit; text-decoration: inherit;">serial_<wbr>number</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A value assigned by the issuer that is unique to a certificate
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="signature_algorithm_python">
<a href="#signature_algorithm_python" style="color: inherit; text-decoration: inherit;">signature_<wbr>algorithm</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The algorithm used to sign the certificate
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updated_at_python">
<a href="#updated_at_python" style="color: inherit; text-decoration: inherit;">updated_<wbr>at</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the certificate was last updated
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-fastly">https://github.com/pulumi/pulumi-fastly</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`fastly` Terraform Provider](https://github.com/fastly/terraform-provider-fastly).{{% /md %}}</dd>
</dl>
