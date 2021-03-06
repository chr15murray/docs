---
title: Module eventgrid
title_tag: Module eventgrid | Package pulumi_azure | Python SDK
linktitle: eventgrid
notitle: true
---

<div class="section" id="eventgrid">
<h1>eventgrid<a class="headerlink" href="#eventgrid" title="Permalink to this headline">¶</a></h1>
<blockquote>
<div><p>This provider is a derived work of the <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-azurerm">Terraform Provider</a> distributed under
<a class="reference external" href="https://www.mozilla.org/en-US/MPL/2.0/">MPL 2.0</a>. If you encounter a bug or missing feature, first check the
<a class="reference external" href="https://github.com/pulumi/pulumi-azure/issues">pulumi/pulumi-azure repo</a>; however, if that doesn’t turn up
anything, please consult the source <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-azurerm/issues">terraform-providers/terraform-provider-azurerm repo</a>.</p>
</div></blockquote>
<span class="target" id="module-pulumi_azure.eventgrid"></span><dl class="py class">
<dt id="pulumi_azure.eventgrid.AwaitableGetTopicResult">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.eventgrid.</code><code class="sig-name descname">AwaitableGetTopicResult</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">endpoint</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">primary_access_key</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">secondary_access_key</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.AwaitableGetTopicResult" title="Permalink to this definition">¶</a></dt>
<dd></dd></dl>

<dl class="py class">
<dt id="pulumi_azure.eventgrid.Domain">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.eventgrid.</code><code class="sig-name descname">Domain</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">input_mapping_default_values</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">input_mapping_fields</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">input_schema</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.Domain" title="Permalink to this definition">¶</a></dt>
<dd><p>Manages an EventGrid Domain</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_azure</span> <span class="k">as</span> <span class="nn">azure</span>

<span class="n">example_resource_group</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">core</span><span class="o">.</span><span class="n">ResourceGroup</span><span class="p">(</span><span class="s2">&quot;exampleResourceGroup&quot;</span><span class="p">,</span> <span class="n">location</span><span class="o">=</span><span class="s2">&quot;West US 2&quot;</span><span class="p">)</span>
<span class="n">example_domain</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">eventgrid</span><span class="o">.</span><span class="n">Domain</span><span class="p">(</span><span class="s2">&quot;exampleDomain&quot;</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">example_resource_group</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">example_resource_group</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">tags</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;environment&quot;</span><span class="p">:</span> <span class="s2">&quot;Production&quot;</span><span class="p">,</span>
    <span class="p">})</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>input_mapping_default_values</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">input_mapping_default_values</span></code> block as defined below.</p></li>
<li><p><strong>input_mapping_fields</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">input_mapping_fields</span></code> block as defined below.</p></li>
<li><p><strong>input_schema</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the schema in which incoming events will be published to this domain. Allowed values are <code class="docutils literal notranslate"><span class="pre">CloudEventSchemaV1_0</span></code>, <code class="docutils literal notranslate"><span class="pre">CustomEventSchema</span></code>, or <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>. Defaults to <code class="docutils literal notranslate"><span class="pre">eventgridschema</span></code>. Changing this forces a new resource to be created.</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the EventGrid Domain resource. Changing this forces a new resource to be created.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the resource group in which the EventGrid Domain exists. Changing this forces a new resource to be created.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>input_mapping_default_values</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">dataVersion</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the default data version of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventType</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the default event type of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subject</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the default subject of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
</ul>
<p>The <strong>input_mapping_fields</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">dataVersion</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the data version of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventTime</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the event time of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventType</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the event type of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">id</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the id of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subject</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the subject of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">topic</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the topic of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
</ul>
<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Domain.endpoint">
<code class="sig-name descname">endpoint</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.endpoint" title="Permalink to this definition">¶</a></dt>
<dd><p>The Endpoint associated with the EventGrid Domain.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Domain.input_mapping_default_values">
<code class="sig-name descname">input_mapping_default_values</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.input_mapping_default_values" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">input_mapping_default_values</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">dataVersion</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the default data version of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventType</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the default event type of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subject</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the default subject of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Domain.input_mapping_fields">
<code class="sig-name descname">input_mapping_fields</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.input_mapping_fields" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">input_mapping_fields</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">dataVersion</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the data version of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventTime</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the event time of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventType</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the event type of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">id</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the id of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subject</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the subject of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">topic</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the topic of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Domain.input_schema">
<code class="sig-name descname">input_schema</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.input_schema" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the schema in which incoming events will be published to this domain. Allowed values are <code class="docutils literal notranslate"><span class="pre">CloudEventSchemaV1_0</span></code>, <code class="docutils literal notranslate"><span class="pre">CustomEventSchema</span></code>, or <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>. Defaults to <code class="docutils literal notranslate"><span class="pre">eventgridschema</span></code>. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Domain.location">
<code class="sig-name descname">location</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.location" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Domain.name">
<code class="sig-name descname">name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the name of the EventGrid Domain resource. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Domain.primary_access_key">
<code class="sig-name descname">primary_access_key</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.primary_access_key" title="Permalink to this definition">¶</a></dt>
<dd><p>The Primary Shared Access Key associated with the EventGrid Domain.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Domain.resource_group_name">
<code class="sig-name descname">resource_group_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.resource_group_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the resource group in which the EventGrid Domain exists. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Domain.secondary_access_key">
<code class="sig-name descname">secondary_access_key</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.secondary_access_key" title="Permalink to this definition">¶</a></dt>
<dd><p>The Secondary Shared Access Key associated with the EventGrid Domain.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Domain.tags">
<code class="sig-name descname">tags</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.tags" title="Permalink to this definition">¶</a></dt>
<dd><p>A mapping of tags to assign to the resource.</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.eventgrid.Domain.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">endpoint</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">input_mapping_default_values</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">input_mapping_fields</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">input_schema</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">primary_access_key</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">secondary_access_key</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing Domain resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>endpoint</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Endpoint associated with the EventGrid Domain.</p></li>
<li><p><strong>input_mapping_default_values</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">input_mapping_default_values</span></code> block as defined below.</p></li>
<li><p><strong>input_mapping_fields</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">input_mapping_fields</span></code> block as defined below.</p></li>
<li><p><strong>input_schema</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the schema in which incoming events will be published to this domain. Allowed values are <code class="docutils literal notranslate"><span class="pre">CloudEventSchemaV1_0</span></code>, <code class="docutils literal notranslate"><span class="pre">CustomEventSchema</span></code>, or <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>. Defaults to <code class="docutils literal notranslate"><span class="pre">eventgridschema</span></code>. Changing this forces a new resource to be created.</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the EventGrid Domain resource. Changing this forces a new resource to be created.</p></li>
<li><p><strong>primary_access_key</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Primary Shared Access Key associated with the EventGrid Domain.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the resource group in which the EventGrid Domain exists. Changing this forces a new resource to be created.</p></li>
<li><p><strong>secondary_access_key</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Secondary Shared Access Key associated with the EventGrid Domain.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>input_mapping_default_values</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">dataVersion</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the default data version of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventType</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the default event type of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subject</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the default subject of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
</ul>
<p>The <strong>input_mapping_fields</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">dataVersion</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the data version of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventTime</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the event time of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventType</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the event type of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">id</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the id of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subject</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the subject of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">topic</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the topic of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
</ul>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.eventgrid.Domain.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.translate_output_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_azure.eventgrid.Domain.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.Domain.translate_input_property" title="Permalink to this definition">¶</a></dt>
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

<dl class="py class">
<dt id="pulumi_azure.eventgrid.DomainTopic">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.eventgrid.</code><code class="sig-name descname">DomainTopic</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">domain_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.DomainTopic" title="Permalink to this definition">¶</a></dt>
<dd><p>Manages an EventGrid Domain Topic</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_azure</span> <span class="k">as</span> <span class="nn">azure</span>

<span class="n">example_resource_group</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">core</span><span class="o">.</span><span class="n">ResourceGroup</span><span class="p">(</span><span class="s2">&quot;exampleResourceGroup&quot;</span><span class="p">,</span> <span class="n">location</span><span class="o">=</span><span class="s2">&quot;West US 2&quot;</span><span class="p">)</span>
<span class="n">example_domain</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">eventgrid</span><span class="o">.</span><span class="n">Domain</span><span class="p">(</span><span class="s2">&quot;exampleDomain&quot;</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">example_resource_group</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">example_resource_group</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">tags</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;environment&quot;</span><span class="p">:</span> <span class="s2">&quot;Production&quot;</span><span class="p">,</span>
    <span class="p">})</span>
<span class="n">example_domain_topic</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">eventgrid</span><span class="o">.</span><span class="n">DomainTopic</span><span class="p">(</span><span class="s2">&quot;exampleDomainTopic&quot;</span><span class="p">,</span>
    <span class="n">domain_name</span><span class="o">=</span><span class="n">example_domain</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">example_resource_group</span><span class="o">.</span><span class="n">name</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>domain_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the EventGrid Domain. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the EventGrid Domain Topic resource. Changing this forces a new resource to be created.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the resource group in which the EventGrid Domain exists. Changing this forces a new resource to be created.</p></li>
</ul>
</dd>
</dl>
<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.DomainTopic.domain_name">
<code class="sig-name descname">domain_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.DomainTopic.domain_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the name of the EventGrid Domain. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.DomainTopic.name">
<code class="sig-name descname">name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.DomainTopic.name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the name of the EventGrid Domain Topic resource. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.DomainTopic.resource_group_name">
<code class="sig-name descname">resource_group_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.DomainTopic.resource_group_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the resource group in which the EventGrid Domain exists. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.eventgrid.DomainTopic.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">domain_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.DomainTopic.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing DomainTopic resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>domain_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the EventGrid Domain. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the EventGrid Domain Topic resource. Changing this forces a new resource to be created.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the resource group in which the EventGrid Domain exists. Changing this forces a new resource to be created.</p></li>
</ul>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.eventgrid.DomainTopic.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.DomainTopic.translate_output_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_azure.eventgrid.DomainTopic.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.DomainTopic.translate_input_property" title="Permalink to this definition">¶</a></dt>
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

<dl class="py class">
<dt id="pulumi_azure.eventgrid.EventSubscription">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.eventgrid.</code><code class="sig-name descname">EventSubscription</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">advanced_filter</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">event_delivery_schema</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">eventhub_endpoint</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">eventhub_endpoint_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">expiration_time_utc</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">hybrid_connection_endpoint</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">hybrid_connection_endpoint_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">included_event_types</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">labels</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">retry_policy</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">scope</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">service_bus_queue_endpoint_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">service_bus_topic_endpoint_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">storage_blob_dead_letter_destination</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">storage_queue_endpoint</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">subject_filter</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">topic_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">webhook_endpoint</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription" title="Permalink to this definition">¶</a></dt>
<dd><p>Manages an EventGrid Event Subscription</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_azure</span> <span class="k">as</span> <span class="nn">azure</span>

<span class="n">default_resource_group</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">core</span><span class="o">.</span><span class="n">ResourceGroup</span><span class="p">(</span><span class="s2">&quot;defaultResourceGroup&quot;</span><span class="p">,</span> <span class="n">location</span><span class="o">=</span><span class="s2">&quot;West US 2&quot;</span><span class="p">)</span>
<span class="n">default_account</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">storage</span><span class="o">.</span><span class="n">Account</span><span class="p">(</span><span class="s2">&quot;defaultAccount&quot;</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">default_resource_group</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">default_resource_group</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">account_tier</span><span class="o">=</span><span class="s2">&quot;Standard&quot;</span><span class="p">,</span>
    <span class="n">account_replication_type</span><span class="o">=</span><span class="s2">&quot;LRS&quot;</span><span class="p">,</span>
    <span class="n">tags</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;environment&quot;</span><span class="p">:</span> <span class="s2">&quot;staging&quot;</span><span class="p">,</span>
    <span class="p">})</span>
<span class="n">default_queue</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">storage</span><span class="o">.</span><span class="n">Queue</span><span class="p">(</span><span class="s2">&quot;defaultQueue&quot;</span><span class="p">,</span> <span class="n">storage_account_name</span><span class="o">=</span><span class="n">default_account</span><span class="o">.</span><span class="n">name</span><span class="p">)</span>
<span class="n">default_event_subscription</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">eventgrid</span><span class="o">.</span><span class="n">EventSubscription</span><span class="p">(</span><span class="s2">&quot;defaultEventSubscription&quot;</span><span class="p">,</span>
    <span class="n">scope</span><span class="o">=</span><span class="n">default_resource_group</span><span class="o">.</span><span class="n">id</span><span class="p">,</span>
    <span class="n">storage_queue_endpoint</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;storage_account_id&quot;</span><span class="p">:</span> <span class="n">default_account</span><span class="o">.</span><span class="n">id</span><span class="p">,</span>
        <span class="s2">&quot;queue_name&quot;</span><span class="p">:</span> <span class="n">default_queue</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="p">})</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>advanced_filter</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">advanced_filter</span></code> block as defined below.</p></li>
<li><p><strong>event_delivery_schema</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the event delivery schema for the event subscription. Possible values include: <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>, <code class="docutils literal notranslate"><span class="pre">CloudEventSchemaV1_0</span></code>, <code class="docutils literal notranslate"><span class="pre">CustomInputSchema</span></code>. Defaults to <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>. Changing this forces a new resource to be created.</p></li>
<li><p><strong>eventhub_endpoint</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">eventhub_endpoint</span></code> block as defined below.</p></li>
<li><p><strong>eventhub_endpoint_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the id where the Event Hub is located.</p></li>
<li><p><strong>expiration_time_utc</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the expiration time of the event subscription (Datetime Format <code class="docutils literal notranslate"><span class="pre">RFC</span> <span class="pre">3339</span></code>).</p></li>
<li><p><strong>hybrid_connection_endpoint</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">hybrid_connection_endpoint</span></code> block as defined below.</p></li>
<li><p><strong>hybrid_connection_endpoint_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the id where the Hybrid Connection is located.</p></li>
<li><p><strong>included_event_types</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – A list of applicable event types that need to be part of the event subscription.</p></li>
<li><p><strong>labels</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – A list of labels to assign to the event subscription.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the EventGrid Event Subscription resource. Changing this forces a new resource to be created.</p></li>
<li><p><strong>retry_policy</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">retry_policy</span></code> block as defined below.</p></li>
<li><p><strong>scope</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the scope at which the EventGrid Event Subscription should be created. Changing this forces a new resource to be created.</p></li>
<li><p><strong>service_bus_queue_endpoint_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the id where the Service Bus Queue is located.</p></li>
<li><p><strong>service_bus_topic_endpoint_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the id where the Service Bus Topic is located.</p></li>
<li><p><strong>storage_blob_dead_letter_destination</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">storage_blob_dead_letter_destination</span></code> block as defined below.</p></li>
<li><p><strong>storage_queue_endpoint</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">storage_queue_endpoint</span></code> block as defined below.</p></li>
<li><p><strong>subject_filter</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">subject_filter</span></code> block as defined below.</p></li>
<li><p><strong>topic_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – (Optional) Specifies the name of the topic to associate with the event subscription.</p></li>
<li><p><strong>webhook_endpoint</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">webhook_endpoint</span></code> block as defined below.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>advanced_filter</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">boolEquals</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using a single boolean value.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[bool]</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberGreaterThanOrEquals</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using a single floating point number.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberGreaterThans</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using a single floating point number.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberIns</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple floating point numbers.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberLessThanOrEquals</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using a single floating point number.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberLessThans</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using a single floating point number.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberNotIns</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple floating point numbers.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringBeginsWiths</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringContains</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringEndsWiths</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringIns</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringNotIns</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
</ul>
<p>The <strong>eventhub_endpoint</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">eventhub_id</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the id of the eventhub where the Event Subscription will receive events.</p></li>
</ul>
<p>The <strong>hybrid_connection_endpoint</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">hybridConnectionId</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the id of the hybrid connection where the Event Subscription will receive events.</p></li>
</ul>
<p>The <strong>retry_policy</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">eventTimeToLive</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies the time to live (in minutes) for events.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">maxDeliveryAttempts</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies the maximum number of delivery retry attempts for events.</p></li>
</ul>
<p>The <strong>storage_blob_dead_letter_destination</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">storage_account_id</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the id of the storage account id where the storage blob is located.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">storageBlobContainerName</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the name of the Storage blob container that is the destination of the deadletter events.</p></li>
</ul>
<p>The <strong>storage_queue_endpoint</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">queue_name</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the name of the storage queue where the Event Subscription will receive events.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">storage_account_id</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the id of the storage account id where the storage queue is located.</p></li>
</ul>
<p>The <strong>subject_filter</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">caseSensitive</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[bool]</span></code>) - Specifies if <code class="docutils literal notranslate"><span class="pre">subject_begins_with</span></code> and <code class="docutils literal notranslate"><span class="pre">subject_ends_with</span></code> case sensitive. This value defaults to <code class="docutils literal notranslate"><span class="pre">false</span></code>.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subjectBeginsWith</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - A string to filter events for an event subscription based on a resource path prefix.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subjectEndsWith</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - A string to filter events for an event subscription based on a resource path suffix.</p></li>
</ul>
<p>The <strong>webhook_endpoint</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">url</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the url of the webhook where the Event Subscription will receive events.</p></li>
</ul>
<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.advanced_filter">
<code class="sig-name descname">advanced_filter</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.advanced_filter" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">advanced_filter</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">boolEquals</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Compares a value of an event using a single boolean value.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">bool</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberGreaterThanOrEquals</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Compares a value of an event using a single floating point number.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberGreaterThans</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Compares a value of an event using a single floating point number.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberIns</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Compares a value of an event using multiple floating point numbers.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberLessThanOrEquals</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Compares a value of an event using a single floating point number.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberLessThans</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Compares a value of an event using a single floating point number.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberNotIns</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Compares a value of an event using multiple floating point numbers.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringBeginsWiths</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringContains</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringEndsWiths</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringIns</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringNotIns</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.event_delivery_schema">
<code class="sig-name descname">event_delivery_schema</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.event_delivery_schema" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the event delivery schema for the event subscription. Possible values include: <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>, <code class="docutils literal notranslate"><span class="pre">CloudEventSchemaV1_0</span></code>, <code class="docutils literal notranslate"><span class="pre">CustomInputSchema</span></code>. Defaults to <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.eventhub_endpoint">
<code class="sig-name descname">eventhub_endpoint</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.eventhub_endpoint" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">eventhub_endpoint</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">eventhub_id</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the id of the eventhub where the Event Subscription will receive events.</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.eventhub_endpoint_id">
<code class="sig-name descname">eventhub_endpoint_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.eventhub_endpoint_id" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the id where the Event Hub is located.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.expiration_time_utc">
<code class="sig-name descname">expiration_time_utc</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.expiration_time_utc" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the expiration time of the event subscription (Datetime Format <code class="docutils literal notranslate"><span class="pre">RFC</span> <span class="pre">3339</span></code>).</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.hybrid_connection_endpoint">
<code class="sig-name descname">hybrid_connection_endpoint</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.hybrid_connection_endpoint" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">hybrid_connection_endpoint</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">hybridConnectionId</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the id of the hybrid connection where the Event Subscription will receive events.</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.hybrid_connection_endpoint_id">
<code class="sig-name descname">hybrid_connection_endpoint_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.hybrid_connection_endpoint_id" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the id where the Hybrid Connection is located.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.included_event_types">
<code class="sig-name descname">included_event_types</code><em class="property">: pulumi.Output[list]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.included_event_types" title="Permalink to this definition">¶</a></dt>
<dd><p>A list of applicable event types that need to be part of the event subscription.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.labels">
<code class="sig-name descname">labels</code><em class="property">: pulumi.Output[list]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.labels" title="Permalink to this definition">¶</a></dt>
<dd><p>A list of labels to assign to the event subscription.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.name">
<code class="sig-name descname">name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the name of the EventGrid Event Subscription resource. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.retry_policy">
<code class="sig-name descname">retry_policy</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.retry_policy" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">retry_policy</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">eventTimeToLive</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - Specifies the time to live (in minutes) for events.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">maxDeliveryAttempts</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - Specifies the maximum number of delivery retry attempts for events.</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.scope">
<code class="sig-name descname">scope</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.scope" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the scope at which the EventGrid Event Subscription should be created. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.service_bus_queue_endpoint_id">
<code class="sig-name descname">service_bus_queue_endpoint_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.service_bus_queue_endpoint_id" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the id where the Service Bus Queue is located.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.service_bus_topic_endpoint_id">
<code class="sig-name descname">service_bus_topic_endpoint_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.service_bus_topic_endpoint_id" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the id where the Service Bus Topic is located.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.storage_blob_dead_letter_destination">
<code class="sig-name descname">storage_blob_dead_letter_destination</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.storage_blob_dead_letter_destination" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">storage_blob_dead_letter_destination</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">storage_account_id</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the id of the storage account id where the storage blob is located.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">storageBlobContainerName</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the name of the Storage blob container that is the destination of the deadletter events.</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.storage_queue_endpoint">
<code class="sig-name descname">storage_queue_endpoint</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.storage_queue_endpoint" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">storage_queue_endpoint</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">queue_name</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the name of the storage queue where the Event Subscription will receive events.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">storage_account_id</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the id of the storage account id where the storage queue is located.</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.subject_filter">
<code class="sig-name descname">subject_filter</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.subject_filter" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">subject_filter</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">caseSensitive</span></code> (<code class="docutils literal notranslate"><span class="pre">bool</span></code>) - Specifies if <code class="docutils literal notranslate"><span class="pre">subject_begins_with</span></code> and <code class="docutils literal notranslate"><span class="pre">subject_ends_with</span></code> case sensitive. This value defaults to <code class="docutils literal notranslate"><span class="pre">false</span></code>.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subjectBeginsWith</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - A string to filter events for an event subscription based on a resource path prefix.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subjectEndsWith</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - A string to filter events for an event subscription based on a resource path suffix.</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.topic_name">
<code class="sig-name descname">topic_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.topic_name" title="Permalink to this definition">¶</a></dt>
<dd><p>(Optional) Specifies the name of the topic to associate with the event subscription.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.EventSubscription.webhook_endpoint">
<code class="sig-name descname">webhook_endpoint</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.webhook_endpoint" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">webhook_endpoint</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">url</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the url of the webhook where the Event Subscription will receive events.</p></li>
</ul>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.eventgrid.EventSubscription.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">advanced_filter</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">event_delivery_schema</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">eventhub_endpoint</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">eventhub_endpoint_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">expiration_time_utc</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">hybrid_connection_endpoint</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">hybrid_connection_endpoint_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">included_event_types</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">labels</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">retry_policy</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">scope</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">service_bus_queue_endpoint_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">service_bus_topic_endpoint_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">storage_blob_dead_letter_destination</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">storage_queue_endpoint</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">subject_filter</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">topic_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">webhook_endpoint</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing EventSubscription resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>advanced_filter</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">advanced_filter</span></code> block as defined below.</p></li>
<li><p><strong>event_delivery_schema</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the event delivery schema for the event subscription. Possible values include: <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>, <code class="docutils literal notranslate"><span class="pre">CloudEventSchemaV1_0</span></code>, <code class="docutils literal notranslate"><span class="pre">CustomInputSchema</span></code>. Defaults to <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>. Changing this forces a new resource to be created.</p></li>
<li><p><strong>eventhub_endpoint</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">eventhub_endpoint</span></code> block as defined below.</p></li>
<li><p><strong>eventhub_endpoint_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the id where the Event Hub is located.</p></li>
<li><p><strong>expiration_time_utc</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the expiration time of the event subscription (Datetime Format <code class="docutils literal notranslate"><span class="pre">RFC</span> <span class="pre">3339</span></code>).</p></li>
<li><p><strong>hybrid_connection_endpoint</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">hybrid_connection_endpoint</span></code> block as defined below.</p></li>
<li><p><strong>hybrid_connection_endpoint_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the id where the Hybrid Connection is located.</p></li>
<li><p><strong>included_event_types</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – A list of applicable event types that need to be part of the event subscription.</p></li>
<li><p><strong>labels</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – A list of labels to assign to the event subscription.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the EventGrid Event Subscription resource. Changing this forces a new resource to be created.</p></li>
<li><p><strong>retry_policy</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">retry_policy</span></code> block as defined below.</p></li>
<li><p><strong>scope</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the scope at which the EventGrid Event Subscription should be created. Changing this forces a new resource to be created.</p></li>
<li><p><strong>service_bus_queue_endpoint_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the id where the Service Bus Queue is located.</p></li>
<li><p><strong>service_bus_topic_endpoint_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the id where the Service Bus Topic is located.</p></li>
<li><p><strong>storage_blob_dead_letter_destination</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">storage_blob_dead_letter_destination</span></code> block as defined below.</p></li>
<li><p><strong>storage_queue_endpoint</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">storage_queue_endpoint</span></code> block as defined below.</p></li>
<li><p><strong>subject_filter</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">subject_filter</span></code> block as defined below.</p></li>
<li><p><strong>topic_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – (Optional) Specifies the name of the topic to associate with the event subscription.</p></li>
<li><p><strong>webhook_endpoint</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">webhook_endpoint</span></code> block as defined below.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>advanced_filter</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">boolEquals</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using a single boolean value.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[bool]</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberGreaterThanOrEquals</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using a single floating point number.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberGreaterThans</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using a single floating point number.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberIns</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple floating point numbers.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberLessThanOrEquals</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using a single floating point number.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberLessThans</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using a single floating point number.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies a single value to compare to when using a single value operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">numberNotIns</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple floating point numbers.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringBeginsWiths</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringContains</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringEndsWiths</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringIns</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">stringNotIns</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Compares a value of an event using multiple string values.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">key</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the field within the event data that you want to use for filtering. Type of the field can be a number, boolean, or string.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">values</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Specifies an array of values to compare to when using a multiple values operator.</p></li>
</ul>
</li>
</ul>
<p>The <strong>eventhub_endpoint</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">eventhub_id</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the id of the eventhub where the Event Subscription will receive events.</p></li>
</ul>
<p>The <strong>hybrid_connection_endpoint</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">hybridConnectionId</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the id of the hybrid connection where the Event Subscription will receive events.</p></li>
</ul>
<p>The <strong>retry_policy</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">eventTimeToLive</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies the time to live (in minutes) for events.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">maxDeliveryAttempts</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies the maximum number of delivery retry attempts for events.</p></li>
</ul>
<p>The <strong>storage_blob_dead_letter_destination</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">storage_account_id</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the id of the storage account id where the storage blob is located.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">storageBlobContainerName</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the name of the Storage blob container that is the destination of the deadletter events.</p></li>
</ul>
<p>The <strong>storage_queue_endpoint</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">queue_name</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the name of the storage queue where the Event Subscription will receive events.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">storage_account_id</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the id of the storage account id where the storage queue is located.</p></li>
</ul>
<p>The <strong>subject_filter</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">caseSensitive</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[bool]</span></code>) - Specifies if <code class="docutils literal notranslate"><span class="pre">subject_begins_with</span></code> and <code class="docutils literal notranslate"><span class="pre">subject_ends_with</span></code> case sensitive. This value defaults to <code class="docutils literal notranslate"><span class="pre">false</span></code>.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subjectBeginsWith</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - A string to filter events for an event subscription based on a resource path prefix.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subjectEndsWith</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - A string to filter events for an event subscription based on a resource path suffix.</p></li>
</ul>
<p>The <strong>webhook_endpoint</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">url</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the url of the webhook where the Event Subscription will receive events.</p></li>
</ul>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.eventgrid.EventSubscription.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.translate_output_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_azure.eventgrid.EventSubscription.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.EventSubscription.translate_input_property" title="Permalink to this definition">¶</a></dt>
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

<dl class="py class">
<dt id="pulumi_azure.eventgrid.GetTopicResult">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.eventgrid.</code><code class="sig-name descname">GetTopicResult</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">endpoint</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">primary_access_key</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">secondary_access_key</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.GetTopicResult" title="Permalink to this definition">¶</a></dt>
<dd><p>A collection of values returned by getTopic.</p>
<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.GetTopicResult.endpoint">
<code class="sig-name descname">endpoint</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.GetTopicResult.endpoint" title="Permalink to this definition">¶</a></dt>
<dd><p>The Endpoint associated with the EventGrid Topic.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.GetTopicResult.id">
<code class="sig-name descname">id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.GetTopicResult.id" title="Permalink to this definition">¶</a></dt>
<dd><p>The provider-assigned unique ID for this managed resource.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.GetTopicResult.primary_access_key">
<code class="sig-name descname">primary_access_key</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.GetTopicResult.primary_access_key" title="Permalink to this definition">¶</a></dt>
<dd><p>The Primary Shared Access Key associated with the EventGrid Topic.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.GetTopicResult.secondary_access_key">
<code class="sig-name descname">secondary_access_key</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.GetTopicResult.secondary_access_key" title="Permalink to this definition">¶</a></dt>
<dd><p>The Secondary Shared Access Key associated with the EventGrid Topic.</p>
</dd></dl>

</dd></dl>

<dl class="py class">
<dt id="pulumi_azure.eventgrid.Topic">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.eventgrid.</code><code class="sig-name descname">Topic</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">input_mapping_default_values</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">input_mapping_fields</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">input_schema</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.Topic" title="Permalink to this definition">¶</a></dt>
<dd><p>Manages an EventGrid Topic</p>
<blockquote>
<div><p><strong>Note:</strong> at this time EventGrid Topic’s are only available in a limited number of regions.</p>
</div></blockquote>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_azure</span> <span class="k">as</span> <span class="nn">azure</span>

<span class="n">example_resource_group</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">core</span><span class="o">.</span><span class="n">ResourceGroup</span><span class="p">(</span><span class="s2">&quot;exampleResourceGroup&quot;</span><span class="p">,</span> <span class="n">location</span><span class="o">=</span><span class="s2">&quot;West US 2&quot;</span><span class="p">)</span>
<span class="n">example_topic</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">eventgrid</span><span class="o">.</span><span class="n">Topic</span><span class="p">(</span><span class="s2">&quot;exampleTopic&quot;</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">example_resource_group</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">example_resource_group</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">tags</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;environment&quot;</span><span class="p">:</span> <span class="s2">&quot;Production&quot;</span><span class="p">,</span>
    <span class="p">})</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>input_mapping_default_values</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">input_mapping_default_values</span></code> block as defined below.</p></li>
<li><p><strong>input_mapping_fields</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">input_mapping_fields</span></code> block as defined below.</p></li>
<li><p><strong>input_schema</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the schema in which incoming events will be published to this domain. Allowed values are <code class="docutils literal notranslate"><span class="pre">CloudEventSchemaV1_0</span></code>, <code class="docutils literal notranslate"><span class="pre">CustomEventSchema</span></code>, or <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>. Defaults to <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>. Changing this forces a new resource to be created.</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the EventGrid Topic resource. Changing this forces a new resource to be created.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the resource group in which the EventGrid Topic exists. Changing this forces a new resource to be created.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>input_mapping_default_values</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">dataVersion</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the default data version of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventType</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the default event type of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subject</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the default subject of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
</ul>
<p>The <strong>input_mapping_fields</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">dataVersion</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the data version of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventTime</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the event time of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventType</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the event type of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">id</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the id of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subject</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the subject of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">topic</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the topic of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
</ul>
<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Topic.endpoint">
<code class="sig-name descname">endpoint</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.endpoint" title="Permalink to this definition">¶</a></dt>
<dd><p>The Endpoint associated with the EventGrid Topic.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Topic.input_mapping_default_values">
<code class="sig-name descname">input_mapping_default_values</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.input_mapping_default_values" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">input_mapping_default_values</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">dataVersion</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the default data version of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventType</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the default event type of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subject</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the default subject of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Topic.input_mapping_fields">
<code class="sig-name descname">input_mapping_fields</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.input_mapping_fields" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">input_mapping_fields</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">dataVersion</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the data version of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventTime</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the event time of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventType</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the event type of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">id</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the id of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subject</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the subject of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">topic</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies the topic of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Topic.input_schema">
<code class="sig-name descname">input_schema</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.input_schema" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the schema in which incoming events will be published to this domain. Allowed values are <code class="docutils literal notranslate"><span class="pre">CloudEventSchemaV1_0</span></code>, <code class="docutils literal notranslate"><span class="pre">CustomEventSchema</span></code>, or <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>. Defaults to <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Topic.location">
<code class="sig-name descname">location</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.location" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Topic.name">
<code class="sig-name descname">name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the name of the EventGrid Topic resource. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Topic.primary_access_key">
<code class="sig-name descname">primary_access_key</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.primary_access_key" title="Permalink to this definition">¶</a></dt>
<dd><p>The Primary Shared Access Key associated with the EventGrid Topic.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Topic.resource_group_name">
<code class="sig-name descname">resource_group_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.resource_group_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the resource group in which the EventGrid Topic exists. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Topic.secondary_access_key">
<code class="sig-name descname">secondary_access_key</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.secondary_access_key" title="Permalink to this definition">¶</a></dt>
<dd><p>The Secondary Shared Access Key associated with the EventGrid Topic.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.eventgrid.Topic.tags">
<code class="sig-name descname">tags</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.tags" title="Permalink to this definition">¶</a></dt>
<dd></dd></dl>

<dl class="py method">
<dt id="pulumi_azure.eventgrid.Topic.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">endpoint</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">input_mapping_default_values</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">input_mapping_fields</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">input_schema</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">primary_access_key</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">secondary_access_key</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing Topic resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>endpoint</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Endpoint associated with the EventGrid Topic.</p></li>
<li><p><strong>input_mapping_default_values</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">input_mapping_default_values</span></code> block as defined below.</p></li>
<li><p><strong>input_mapping_fields</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">input_mapping_fields</span></code> block as defined below.</p></li>
<li><p><strong>input_schema</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the schema in which incoming events will be published to this domain. Allowed values are <code class="docutils literal notranslate"><span class="pre">CloudEventSchemaV1_0</span></code>, <code class="docutils literal notranslate"><span class="pre">CustomEventSchema</span></code>, or <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>. Defaults to <code class="docutils literal notranslate"><span class="pre">EventGridSchema</span></code>. Changing this forces a new resource to be created.</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the EventGrid Topic resource. Changing this forces a new resource to be created.</p></li>
<li><p><strong>primary_access_key</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Primary Shared Access Key associated with the EventGrid Topic.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the resource group in which the EventGrid Topic exists. Changing this forces a new resource to be created.</p></li>
<li><p><strong>secondary_access_key</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Secondary Shared Access Key associated with the EventGrid Topic.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>input_mapping_default_values</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">dataVersion</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the default data version of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventType</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the default event type of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subject</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the default subject of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
</ul>
<p>The <strong>input_mapping_fields</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">dataVersion</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the data version of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventTime</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the event time of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">eventType</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the event type of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">id</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the id of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">subject</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the subject of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">topic</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies the topic of the EventGrid Event to associate with the domain. Changing this forces a new resource to be created.</p></li>
</ul>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.eventgrid.Topic.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.translate_output_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_azure.eventgrid.Topic.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.Topic.translate_input_property" title="Permalink to this definition">¶</a></dt>
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

<dl class="py function">
<dt id="pulumi_azure.eventgrid.get_topic">
<code class="sig-prename descclassname">pulumi_azure.eventgrid.</code><code class="sig-name descname">get_topic</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.eventgrid.get_topic" title="Permalink to this definition">¶</a></dt>
<dd><p>Use this data source to access information about an existing EventGrid Topic</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_azure</span> <span class="k">as</span> <span class="nn">azure</span>

<span class="n">example</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">eventgrid</span><span class="o">.</span><span class="n">get_topic</span><span class="p">(</span><span class="n">name</span><span class="o">=</span><span class="s2">&quot;my-eventgrid-topic&quot;</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="s2">&quot;example-resources&quot;</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>name</strong> (<em>str</em>) – The name of the EventGrid Topic resource.</p></li>
<li><p><strong>resource_group_name</strong> (<em>str</em>) – The name of the resource group in which the EventGrid Topic exists.</p></li>
</ul>
</dd>
</dl>
</dd></dl>

</div>
