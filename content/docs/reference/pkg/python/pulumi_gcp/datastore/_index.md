---
title: Module datastore
title_tag: Module datastore | Package pulumi_gcp | Python SDK
linktitle: datastore
notitle: true
---

{{< resource-docs-alert "gcp" >}}

<div class="section" id="datastore">
<h1>datastore<a class="headerlink" href="#datastore" title="Permalink to this headline">¶</a></h1>
<blockquote>
<div><p>This provider is a derived work of the <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-google">Terraform Provider</a> distributed under
<a class="reference external" href="https://www.mozilla.org/en-US/MPL/2.0/">MPL 2.0</a>. If you encounter a bug or missing feature, first check the
<a class="reference external" href="https://github.com/pulumi/pulumi-gcp/issues">pulumi/pulumi-gcp repo</a>; however, if that doesn’t turn up
anything, please consult the source <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-google/issues">terraform-providers/terraform-provider-google repo</a>.</p>
</div></blockquote>
<span class="target" id="module-pulumi_gcp.datastore"></span><dl class="py class">
<dt id="pulumi_gcp.datastore.DataStoreIndex">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_gcp.datastore.</code><code class="sig-name descname">DataStoreIndex</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">ancestor</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">kind</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">project</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">properties</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.datastore.DataStoreIndex" title="Permalink to this definition">¶</a></dt>
<dd><p>Describes a composite index for Cloud Datastore.</p>
<p>To get more information about Index, see:</p>
<ul class="simple">
<li><p><a class="reference external" href="https://cloud.google.com/datastore/docs/reference/admin/rest/v1/projects.indexes">API documentation</a></p></li>
<li><p>How-to Guides</p>
<ul>
<li><p><a class="reference external" href="https://cloud.google.com/datastore/docs/concepts/indexes">Official Documentation</a></p></li>
</ul>
</li>
</ul>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_gcp</span> <span class="k">as</span> <span class="nn">gcp</span>

<span class="n">default</span> <span class="o">=</span> <span class="n">gcp</span><span class="o">.</span><span class="n">datastore</span><span class="o">.</span><span class="n">DataStoreIndex</span><span class="p">(</span><span class="s2">&quot;default&quot;</span><span class="p">,</span>
    <span class="n">kind</span><span class="o">=</span><span class="s2">&quot;foo&quot;</span><span class="p">,</span>
    <span class="n">properties</span><span class="o">=</span><span class="p">[</span>
        <span class="p">{</span>
            <span class="s2">&quot;direction&quot;</span><span class="p">:</span> <span class="s2">&quot;ASCENDING&quot;</span><span class="p">,</span>
            <span class="s2">&quot;name&quot;</span><span class="p">:</span> <span class="s2">&quot;property_a&quot;</span><span class="p">,</span>
        <span class="p">},</span>
        <span class="p">{</span>
            <span class="s2">&quot;direction&quot;</span><span class="p">:</span> <span class="s2">&quot;ASCENDING&quot;</span><span class="p">,</span>
            <span class="s2">&quot;name&quot;</span><span class="p">:</span> <span class="s2">&quot;property_b&quot;</span><span class="p">,</span>
        <span class="p">},</span>
    <span class="p">])</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>ancestor</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Policy for including ancestors in the index.</p></li>
<li><p><strong>kind</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The entity kind which the index applies to.</p></li>
<li><p><strong>project</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.</p></li>
<li><p><strong>properties</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – An ordered list of properties to index on.  Structure is documented below.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>properties</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">direction</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The direction the index should optimize for sorting.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">name</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The property name to index.</p></li>
</ul>
<dl class="py attribute">
<dt id="pulumi_gcp.datastore.DataStoreIndex.ancestor">
<code class="sig-name descname">ancestor</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.datastore.DataStoreIndex.ancestor" title="Permalink to this definition">¶</a></dt>
<dd><p>Policy for including ancestors in the index.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_gcp.datastore.DataStoreIndex.index_id">
<code class="sig-name descname">index_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.datastore.DataStoreIndex.index_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The index id.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_gcp.datastore.DataStoreIndex.kind">
<code class="sig-name descname">kind</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.datastore.DataStoreIndex.kind" title="Permalink to this definition">¶</a></dt>
<dd><p>The entity kind which the index applies to.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_gcp.datastore.DataStoreIndex.project">
<code class="sig-name descname">project</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.datastore.DataStoreIndex.project" title="Permalink to this definition">¶</a></dt>
<dd><p>The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_gcp.datastore.DataStoreIndex.properties">
<code class="sig-name descname">properties</code><em class="property">: pulumi.Output[list]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.datastore.DataStoreIndex.properties" title="Permalink to this definition">¶</a></dt>
<dd><p>An ordered list of properties to index on.  Structure is documented below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">direction</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The direction the index should optimize for sorting.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">name</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The property name to index.</p></li>
</ul>
</dd></dl>

<dl class="py method">
<dt id="pulumi_gcp.datastore.DataStoreIndex.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">ancestor</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">index_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">kind</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">project</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">properties</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.datastore.DataStoreIndex.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing DataStoreIndex resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>ancestor</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Policy for including ancestors in the index.</p></li>
<li><p><strong>index_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The index id.</p></li>
<li><p><strong>kind</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The entity kind which the index applies to.</p></li>
<li><p><strong>project</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.</p></li>
<li><p><strong>properties</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – An ordered list of properties to index on.  Structure is documented below.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>properties</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">direction</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The direction the index should optimize for sorting.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">name</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The property name to index.</p></li>
</ul>
</dd></dl>

<dl class="py method">
<dt id="pulumi_gcp.datastore.DataStoreIndex.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.datastore.DataStoreIndex.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_gcp.datastore.DataStoreIndex.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.datastore.DataStoreIndex.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

</dd></dl>

</div>
