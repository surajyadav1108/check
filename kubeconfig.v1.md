---
title: kube 配置 (v1)
content_type: tool-reference
package: v1
---

<!--
title: kubeconfig (v1)
content_type: tool-reference
package: v1
auto_generated: true
-->

<!--
## Resource Types
-->
## 资源类型 


- [Config  配置](#Config)
  
    
    

## `Config`     {#Config}
    
<!--
Config holds the information needed to build connect to remote kubernetes clusters as a given user
-->
<p>config 保存以给定用户身份构建连接到远程 Kubernetes 集群所需的信息 </p>


<table class="table">
<thead><tr><th width="30%"><!--Field-->字段</th><th><!--Description-->描述</th></tr></thead>
<tbody>
    
<tr><td><code>apiVersion</code><br/>string</td><td><code>/v1</code></td></tr>
<tr><td><code>kind</code><br/>string</td><td><code>Config</code></td></tr>
    
  
<tr><td><code>kind</code><br/>
<code>string</code>
</td>
<td>
  <!--
  Legacy field from pkg/api/types.go TypeMeta.TODO(jlowdermilk): remove this after eliminating downstream dependencies.
  -->
   <p>来自 pkg/api/types.go 的遗留字段 TypeMeta.
TODO(jlowdermilk): 在消除下游依赖后删除这个.</p>
</td>
</tr>
<tr><td><code>apiVersion</code><br/>
<code>string</code>
</td>
<td>
  <!---
  Legacy field from pkg/api/types.go TypeMeta. TODO(jlowdermilk): remove this after eliminating downstream dependencies.
  -->
   <p>来自 pkg/api/types.go 的遗留字段 TypeMeta.
TODO(jlowdermilk): 在消除下游依赖后删除这个.</p>
</td>
</tr>
<tr><td><code>preferences</code><B><!--[Required]-->[必需]</B><br/>
<a href="#Preferences"><code>Preferences</code></a>
</td>
<td>
  <!--
  Preferences holds general information to be use for cli interactions.
  -->
   <p><code>Preferences</code>保存用于 CLI 交互的一般信息</p>
</td>
</tr>
<tr><td><code>clusters</code><B><!--[Required]-->[必需]</B><br/>
<a href="#NamedCluster"><code>[]NamedCluster</code></a>
</td>
<td>
  <!---
  Clusters is a map of referencable names to cluster configs.
  -->
   <p><code>Clusters</code> 是可引用名称到集群配置的映射</p>
</td>
</tr>
<tr><td><code>users</code><B><!--[Required]-->[必需]</B><br/>
<a href="#NamedAuthInfo"><code>[]NamedAuthInfo</code></a>
</td>
<td>
  <!--
  AuthInfos is a map of referencable names to user configs.
  -->
   <p><code>AuthInfos</code> 是一个从可引用名称到用户配置的映射</p>
</td>
</tr>
<tr><td><code>contexts</code><B><!--[Required]-->[必需]</B><br/>
<a href="#NamedContext"><code>[]NamedContext</code></a>
</td>
<td>
  <!--
  Contexts is a map of referencable names to context configs.
  -->
   <p><code>Contexts</code> 是上下文配置的引用名称的地图.</p>
</td>
</tr>
<tr><td><code>current-context</code><B><!--[Required]-->[必需]</B><br/>
<code>string</code>
</td>
<td>
  <!---
  CurrentContext is the name of the context that you would like to use by default.
  --->
   <p><code>CurrentContext</code> 是默认情况下你想使用的上下文的名称。</p>
</td>
</tr>
<tr><td><code>extensions</code><br/>
<a href="#NamedExtension"><code>[]NamedExtension</code></a>
</td>
<td>
  <!--
  Extensions holds additional information. This is useful for extenders so that reads and writes don't clobber unknown fields.
  -->
   <p><code>Extensions</code> 保存额外信息. 这对于扩展器是有用的，这样读写不会破解未知字段.</p>
</td>
</tr>
</tbody>
</table>

## `AuthInfo`     {#AuthInfo}
    
<!--
**Appears in:**
-->
**出现在:**

- [NamedAuthInfo](#NamedAuthInfo)

<!--
AuthInfo contains information that describes identity information.  This is use to tell the kubernetes cluster who you are.
-->
<p>AuthInfo 包含描述身份信息的信息. 这用来告诉 kubernetes 集群你是谁.</p>


<table class="table">
<thead><tr><th width="30%"><!--Field-->字段</th><th><!--Description-->描述</th></tr></thead>
<tbody>
    
  
<tr><td><code>client-certificate</code><br/>
<code>string</code>
</td>
<td>
  <!--
  ClientCertificate is the path to a client cert file for TLS
  -->
   <p><code>ClientCertificate</code> 是TLS客户端证书文件的路径.</p>
</td>
</tr>
<tr><td><code>client-certificate-data</code><br/>
<code>[]byte</code>
</td>
<td>
  <!--
  ClientCertificateData contains PEM-encoded data from a client cert file for TLS. Overrides ClientCertificate
  -->
   <p><code>ClientCertificateData</code> 包含PEM编码的数据 从 <code>TLS</code> 的客户端证书文件. 覆盖 <code>ClientCertificate</code></p>
</td>
</tr>
<tr><td><code>client-key</code><br/>
<code>string</code>
</td>
<td>
  <!--
  ClientKey is the path to a client key file for TLS
  -->
   <p><code>ClientKey</code> 是用于 <code>TLS</code> 的客户端密钥文件的路径.</p>
</td>
</tr>
<tr><td><code>client-key-data</code><br/>
<code>[]byte</code>
</td>
<td>
  <!--
  ClientKeyData contains PEM-encoded data from a client key file for TLS. Overrides ClientKey
  --->
   <p><code>ClientKeyData</code> 包含来自 <code>TLS</code> 客户端密钥文件的 <code>PEM</code> 编码数据. 覆盖 <code>ClientKey</code></p>
</td>
</tr>
<tr><td><code>token</code><br/>
<code>string</code>
</td>
<td>
  <!--
  Token is the bearer token for authentication to the kubernetes cluster
  --->
   <p><code>Token</code> 是用于对<code>kubernetes</code>集群进行身份验证的持有者代币.</p>
</td>
</tr>
<tr><td><code>tokenFile</code><br/>
<code>string</code>
</td>
<td>
  <!--
  TokenFile is a pointer to a file that contains a bearer token (as described above).  If both Token and TokenFile are present, Token takes precedence.
  -->
   <p><code>TokenFile</code> 是指指包含有bearer代币的文件的指针 (如上所述). 如果两个<code>Token</code>和<code>Token file</code>都存在，<code>Token</code>优先.</p>
</td>
</tr>
<tr><td><code>as</code><br/>
<code>string</code>
</td>
<td>
  <!--
  Impersonate is the username to impersonate.  The name matches the flag.
  -->
   <p><code>Impersonate</code> 是要模仿的用户名. 名字与国旗相匹配.</p>
</td>
</tr>
<tr><td><code>as-uid</code><br/>
<code>string</code>
</td>
<td>
  <!--
  ImpersonateUID is the uid to impersonate.
  -->
   <p><code>ImpersonateUID</code> 就是 uid 为了冒充.</p>
</td>
</tr>
<tr><td><code>as-groups</code><br/>
<code>[]string</code>
</td>
<td>
  <!--
  ImpersonateGroups is the groups to impersonate.
  --->
   <p><code>ImpersonateGroups</code> 就是 要冒充的组.</p>
</td>
</tr>
<tr><td><code>as-user-extra</code><br/>
<code>map[string][]string</code>
</td>
<td>
  <!--
  ImpersonateUserExtra contains additional information for impersonated user.
  --->
   <p><code>ImpersonateUserExtra</code> 包含给模拟用户的额外信息.</p>
</td>
</tr>
<tr><td><code>username</code><br/>
<code>string</code>
</td>
<td>
  <!---
  Username is the username for basic authentication to the kubernetes cluster.
  --->
   <p><code>Username</code> 是对<code>kubernetes</code> 集群进行基本认证的用户名.</p>
</td>
</tr>
<tr><td><code>password</code><br/>
<code>string</code>
</td>
<td>
  <!---
  Password is the password for basic authentication to the kubernetes cluster.
  --->
   <p><code>Password</code> 是对 <code>kubernetes</code> 集群进行基本认证的密码.</p>
</td>
</tr>
<tr><td><code>auth-provider</code><br/>
<a href="#AuthProviderConfig"><code>AuthProviderConfig</code></a>
</td>
<td>
  <!---
  AuthProvider specifies a custom authentication plugin for the kubernetes cluster.
  --->
   <p><code>AuthProvider</code> 为 <code>kubernetes</code> 集群指定自定义身份验证插件.</p>
</td>
</tr>
<tr><td><code>exec</code><br/>
<a href="#ExecConfig"><code>ExecConfig</code></a>
</td>
<td>
  <!---
  Exec specifies a custom exec-based authentication plugin for the kubernetes cluster.
  --->
   <p><code>Exec</code> 指定了针对 <code>kubernetes</code> 集群的自定义基于 <code>exec</code> 的身份验证插件.</p>
</td>
</tr>
<tr><td><code>extensions</code><br/>
<a href="#NamedExtension"><code>[]NamedExtension</code></a>
</td>
<td>
  <!---
  Extensions holds additional information. This is useful for extenders so that reads and writes don't clobber unknown fields.
  --->
   <p><code>Extensions</code> 保存额外信息. 这对于扩展器是有用的，这样读写不会破解未知字段</p>
</td>
</tr>
</tbody>
</table>

## `AuthProviderConfig`     {#AuthProviderConfig}
    
<!--
**Appears in:**
-->
**出现在:**

- [AuthInfo](#AuthInfo)

<!--
AuthProviderConfig holds the configuration for a specified auth provider.
-->
<p>AuthProviderConfig 保存特定认证提供商的配置.</p>


<table class="table">
<thead><tr><th width="30%"><!--Field-->字段</th><th><!--Description-->描述</th></tr></thead>
<tbody>
    
  
<tr><td><code>name</code><B><!--[Required]-->[必需]</B><br/>
<code>string</code>
</td>
<td>
   <span class="text-muted"><!--No description provided-->环境变量名称.</span></td>
</tr>
<tr><td><code>config</code><B><!--[Required]-->[必需]</B><br/>
<code>map[string]string</code>
</td>
<td>
   <span class="text-muted"><!--No description provided-->环境变量名称.</span></td>
</tr>
</tbody>
</table>

## `Cluster`     {#Cluster}
    
<!--
**Appears in:**
-->
**出现在:**

- [NamedCluster](#NamedCluster)

<!--
Cluster contains information about how to communicate with a kubernetes cluster.
--->
<p>Cluster 包含有关如何与 kubernetes 集群通信的信息</p>


<table class="table">
<thead><tr><th width="30%"><!--Field-->字段</th><th><!--Description-->描述</th></tr></thead>
<tbody>
    
  
<tr><td><code>server</code><B><!--[Required]-->[必需]</B><br/>
<code>string</code>
</td>
<td>
  <!--
  Server is the address of the kubernetes cluster (https://hostname:port).
  --->
   <p><code>Server</code> 是 <code>kubernetes</code> 集群的地址 <code>(https://hostname:port)</code>.</p>
</td>
</tr>
<tr><td><code>tls-server-name</code><br/>
<code>string</code>
</td>
<td>
  <!--
  TLSServerName is used to check server certificate. If TLSServerName is empty, the hostname used to contact the server is used.
  --->
   <p><code>TLSServerName</code> 用于检查服务器证书. 如果 <code>TLSServerName</code> 是空的，则使用用于联系服务器的主机名.</p>
</td>
</tr>
<tr><td><code>insecure-skip-tls-verify</code><br/>
<code>bool</code>
</td>
<td>
  <!---
  InsecureSkipTLSVerify skips the validity check for the server's certificate. This will make your HTTPS connections insecure.
  ---->
   <p><code>InsecureSkipTLSVerify</code> 跳过服务器证书的有效性检查. 这将使您的 HTTPS 连接不安全.</p>
</td>
</tr>
<tr><td><code>certificate-authority</code><br/>
<code>string</code>
</td>
<td>
  <!--
  CertificateAuthority is the path to a cert file for the certificate authority.
  -->
   <p><code>CertificateAuthority</code> 是证书颁发机构的证书文件的路径.</p>
</td>
</tr>
<tr><td><code>certificate-authority-data</code><br/>
<code>[]byte</code>
</td>
<td>
  <!---
  CertificateAuthorityData contains PEM-encoded certificate authority certificates. Overrides CertificateAuthority
  --->
   <p><code>CertificateAuthorityData</code> 包含 <code>PEM-encoded</code> 证书 权威 证书. 覆盖 <code>CertificateAuthority</code></p>
</td>
</tr>
<tr><td><code>proxy-url</code><br/>
<code>string</code>
</td>
<td>
  <!--
  ProxyURL is the URL to the proxy to be used for all requests made by this
client. URLs with &quot;http&quot;, &quot;https&quot;, and &quot;socks5&quot; schemes are supported.  If
this configuration is not provided or the empty string, the client
attempts to construct a proxy configuration from http_proxy and
https_proxy environment variables. If these environment variables are not
set, the client does not attempt to proxy requests.
  -->
  
   <p><code>ProxyURL</code> 是代理用于此客户端的所有请求的 <code>URL</code>. <code>URL</code> 带有的 &quot;<code>http</code>&quot;, &quot;<code>https</code>&quot;, 和 &quot;<code>socks5</code>&quot; 受支持. 如果
未提供此配置或为空字符串, 客户端
尝试从 <code>http_proxy</code> 构建代理配置 和
<code>https_proxy</code> 环境变量. 如果这些环境变量没有设置, 客户端不会尝试代理请求.
   </p>

<!--
socks5 proxying does not currently support spdy streaming endpoints (exec,
attach, port forward).
--->

<p><code>socks5</code> 代理当前不支持 <code>spdy</code> 流式端点（<code>exec</code>、<code>attach</code>、<code>port-forward(端口转发)</code>).</p>
</td>
</tr>
<tr><td><code>disable-compression</code><br/>
<code>bool</code>
</td>
<td>
  <!--
  DisableCompression allows client to opt-out of response compression for all requests to the server. This is useful
to speed up requests (specifically lists) when client-server network bandwidth is ample, by saving time on
compression (server-side) and decompression (client-side): https://github.com/kubernetes/kubernetes/issues/112296.
  -->
  
   <p><code>DisableCompression</code> 允许客户端选择不对发往服务器的所有请求进行响应压缩. 这对于加快请求（具体是列表）非常有用，当客户端与服务器之间的网络带宽充足时, "通过节省时间进行压缩（服务器端）<code>server-side</code> 和解压缩（客户端）<code>client-side</code>：<code>https://github.com/kubernetes/kubernetes/issues/112296</code>.</p>
</td>
</tr>
<tr><td><code>extensions</code><br/>
<a href="#NamedExtension"><code>[]NamedExtension</code></a>
</td>
<td>
  <!--
  Extensions holds additional information. This is useful for extenders so that reads and writes don't clobber unknown fields
  -->
   <p><code>Extensions</code> 保存额外信息. 这对于扩展器是有用的，这样读写不会破解未知字段</p>
</td>
</tr>
</tbody>
</table>

## `Context`     {#Context}
    
<!--
**Appears in:**
-->
**出现在:**

- [NamedContext](#NamedContext)

<!--
Context is a tuple of references to a cluster (how do I communicate with a kubernetes cluster), a user (how do I identify myself), and a namespace (what subset of resources do I want to work with)
-->
<p>上下文是对集群的引用元组 (如何与 <code>Kubernetes</code> 集群通信), 一个用户 (我如何识别自己), 和一个命名空间 (我想要使用哪些资源子集)</p>


<table class="table">
<thead><tr><th width="30%"><!--Field-->字段</th><th><!--Description-->描述</th></tr></thead>
<tbody>
    
  
<tr><td><code>cluster</code><B><!--[Required]-->[必需]</B><br/>
<code>string</code>
</td>
<td>
  <!--
  Cluster is the name of the cluster for this context
  -->
   <p><code>Cluster</code> 是此上下文中的集群名称</p>
</td>
</tr>
<tr><td><code>user</code><B><!--[Required]-->[必需]</B><br/>
<code>string</code>
</td>
<td>
  <!--
  AuthInfo is the name of the authInfo for this context
  --->
   <p><code>AuthInfo</code> 是此上下文的 authInfo 名称</p>
</td>
</tr>
<tr><td><code>namespace</code><br/>
<code>string</code>
</td>
<td>
  <!--
Namespace is the default namespace to use on unspecified requests
  -->
   <p><code>Namespace</code> 是在未指定请求时使用的默认命名空间.</p>
</td>
</tr>
<tr><td><code>extensions</code><br/>
<a href="#NamedExtension"><code>[]NamedExtension</code></a>
</td>
<td>
  <!--
  Extensions holds additional information. This is useful for extenders so that reads and writes don't clobber unknown fields
  -->
   <p><code>Extensions</code> 保存额外信息. 这对于扩展器是有用的，这样读写不会破解未知字段</p>
</td>
</tr>
</tbody>
</table>

## `ExecConfig`     {#ExecConfig}
    
<!--
**Appears in:**
-->
**出现在:**

- [AuthInfo](#AuthInfo)

<!---
ExecConfig specifies a command to provide client credentials. The command is exec'd and outputs structured stdout holding credentials.
See the client.authentication.k8s.io API group for specifications of the exact input and output format
-->

<p><code>ExecConfig</code> 指定提供客户端凭证的命令. 这个命令被执（exec'd）
并输出结构化的标准输出 <code>(stdout)</code>，其中包含了凭据.</p>

<!--
See the client.authentication.k8s.io API group for specifications of the exact input
and output format
-->

<p>查看 <code>client.authentication.k8s.io API</code> 组以获取确切的输入和输出格式规范.</p>

<table class="table">
<thead><tr><th width="30%"><!--Field-->字段</th><th><!--Description-->描述</th></tr></thead>
<tbody>
    
  
<tr><td><code>command</code><B><!--[Required]-->[必需]</B><br/>
<code>string</code>
</td>
<td>
  <!--
  Command to execute.
  --->
   <p>要执行的命令.</p>
</td>
</tr>
<tr><td><code>args</code><br/>
<code>[]string</code>
</td>
<td>
  <!--
  Arguments to pass to the command when executing it.
  -->
   <p>执行命令时要传递的参数.</p>
</td>
</tr>
<tr><td><code>env</code><br/>
<a href="#ExecEnvVar"><code>[]ExecEnvVar</code></a>
</td>
<td>
  <!---
  Env defines additional environment variables to expose to the process. These
are unioned with the host's environment, as well as variables client-go uses
to pass argument to the plugin.
  --->
  
   <p><code>Env</code> 定义了要暴露给进程的额外环境变量. 这些与主机的环境合并在一起, 以及 <code>client-go</code> 用于传递参数给插件的变量.</p>
</td>
</tr>
<tr><td><code>apiVersion</code><B><!--[Required]-->[必需]</B><br/>
<code>string</code>
</td>
<td>
   <!---
  Preferred input version of the ExecInfo. The returned ExecCredentials MUST use
  the same encoding version as the input.
  --->
  
   <p><code>ExecInfo</code> 的首选输入版本. 返回的 <code>ExecCredentials</code> 必须使用与输入相同的编码版本.</p>
</td>
</tr>
<tr><td><code>installHint</code><B><!--[Required]-->[必需]</B><br/>
<code>string</code>
</td>
<td>
  <!--
  This text is shown to the user when the executable doesn't seem to be
  present. For example, <code>brew install foo-cli</code> might be a good InstallHint for
  foo-cli on Mac OS systems
  -->
  
   <p>当似乎找不到可执行文件时，将向用户显示此文本, 例如, <code>brew install foo-cli</code> 这可能是在 <code>Mac OS</code> 系统上安装 <code>foo-cli</code> 的良好提示.</p>
</td>
</tr>
<tr><td><code>provideClusterInfo</code><B><!--[Required]-->[必需]</B><br/>
<code>bool</code>
</td>
<td>
  
  <!---
  ProvideClusterInfo determines whether or not to provide cluster information,
which could potentially contain very large CA data, to this exec plugin as a
part of the KUBERNETES_EXEC_INFO environment variable. By default, it is set
to false. Package k8s.io/client-go/tools/auth/exec provides helper methods for
reading this environment variable
  --->
  
   <p><code>ProvideClusterInfo</code> 决定是否提供集群信息,这些信息可能包含非常大的 <code>CA</code> 数据, 提供给这个执行插件作为 <code>KUBERNETES_EXEC_INFO</code> 环境变量的一部分. 默认情况下，它被设置为 <code>false</code>. <code>k8s.io/client-go/tools/auth/exec</code> 包提供了用于读取这个环境变量的辅助方法.</p>
</td>
</tr>
<tr><td><code>interactiveMode</code><br/>
<a href="#ExecInteractiveMode"><code>ExecInteractiveMode</code></a>
</td>
<td>

  <!---
  InteractiveMode determines this plugin's relationship with standard input. Valid
values are &quot;Never&quot; (this exec plugin never uses standard input), &quot;IfAvailable&quot; (this
exec plugin wants to use standard input if it is available), or &quot;Always&quot; (this exec
plugin requires standard input to function). See ExecInteractiveMode values for more
details.
  -->
  
   <p><code>InteractiveMode</code> 确定此插件与标准输入的关系. 有效值为 &quot;Never(从不)&quot; (这个 <code>exec</code> 插件从不使用标准输入), &quot;<code>IfAvailable</code>(如果可用)&quot; (这个 <code>exec</code> 插件希望使用标准输入，如果它是可用的), 或者 &quot;Always(始终)&quot; (这个 <code>exec</code> 插件需要标准输入以正常运行). 查看<code>ExecInteractiveMode</code> 值以了解更多详情.</p>

<!--
If APIVersion is client.authentication.k8s.io/v1alpha1 or
client.authentication.k8s.io/v1beta1, then this field is optional and defaults
to &quot;IfAvailable&quot; when unset. Otherwise, this field is required.
-->

<p>如果 <code>APIVersion</code> 是 <code>client.authentication.k8s.io/v1alpha1</code> 或 <code>client.authentication.k8s.io/v1beta1</code>, 如果 <code>APIVersion</code> 是  
 <code>client.authentication.k8s.io/v1alpha1</code> 或 <code>client.authentication.k8s.io/v1beta1</code>，则此字段是可选的，当未设置时默认为 &quot;<code>IfAvailable</code>&quot; (未设置 <code>unset</code>). 否则，此字段是必需的.</p>
</td>
</tr>
</tbody>
</table>

## `ExecEnvVar`     {#ExecEnvVar}
    
<!--
**Appears in:**
-->
**出现在:**

- [ExecConfig](#ExecConfig)


<!---
ExecEnvVar is used for setting environment variables when executing an exec-based
credential plugin
-->

<p><code>ExecEnvVar</code> 用于在执行基于 <code>exec</code> 的凭据插件时设置环境变量.</p>


<table class="table">
<thead><tr><th width="30%"><!--Field-->字段</th><th><!--Description-->描述</th></tr></thead>
<tbody>
    
  
<tr><td><code>name</code><br/><B><!--[Required]-->[必需]</B>
<code>string</code>
</td>
<td>
   <span class="text-muted">环境变量名称.</span></td>
</tr>
<tr><td><code>value</code><B></br><!--[Required]-->[必需]</B>
<code>string</code>
</td>
<td>
   <span class="text-muted">环境变量名称.</span></td>
</tr>
</tbody>
</table>

## `ExecInteractiveMode`     {#ExecInteractiveMode}
    
(Alias of `string`)

<!--
**Appears in:**
-->
**Appears in:**

- [ExecConfig](#ExecConfig)

<!--
ExecInteractiveMode is a string that describes an exec plugin's relationship with standard input.
-->

<p>ExecInteractiveMode 是一个描述 exec 插件与标准输入关系的字符串.</p>




## `NamedAuthInfo`     {#NamedAuthInfo}
    
<!--
**Appears in:**
-->
**出现在:**

- [Config](#Config)

<!---
NamedAuthInfo relates nicknames to auth information
-->
<p>'NamedAuthInfo' - 将绰号与auth信息联系起来</p>


<table class="table">
<thead><tr><th width="30%"><!--Field-->字段</th><th><!--Description-->描述</th></tr></thead>
<tbody>
    
  
<tr><td><code>name</code><B><!--[Required]-->[必需]</B>
<code>string</code>
</td>
<td>
  <!--
  Name is the nickname for this AuthInfo
  --->
   <p><code>Name</code> 是该 <code>AuthInfo</code> 的昵称</p>
</td>
</tr>
<tr><td><code>user</code><B><!--[Required]-->[必需]</B><br/>
<a href="#AuthInfo"><code>AuthInfo</code></a>
</td>
<td>
  <!--
  AuthInfo holds the auth information
  --->
   <p><code>AuthInfo</code> 保存认证信息</p>
</td>
</tr>
</tbody>
</table>

## `NamedCluster`     {#NamedCluster}
    
<!--
**Appears in:**
-->
**出现在:**

- [Config](#Config)

<!--
NamedCluster relates nicknames to cluster information
-->
<p>NamedCluster 将昵称与集群信息关联起来.</p>


<table class="table">
<thead><tr><th width="30%"><!--Field-->字段</th><th><!--Description-->描述</th></tr></thead>
<tbody>
    
  
<tr><td><code>name</code><B></br><!--[Required]-->[必需]</B><br/>
<code>string</code>
</td>
<td>
  <!--
  Name is the nickname for this Cluster
  -->
   <p><code>Name</code> 是该集群的昵称.</p>
</td>
</tr>
<tr><td><code>cluster</code><br/><B><!--[Required]-->[必需]</B><br/>
<a href="#Cluster"><code>Cluster</code></a>
</td>
<td>
  <!--
  Cluster holds the cluster information
  -->
   <p><code>Cluster</code> 保存了集群信息</p>
</td>
</tr>
</tbody>
</table>

## `NamedContext`     {#NamedContext}
    
<!--
**Appears in:**
-->
**出现在:**

- [Config](#Config)

<!--
NamedContext relates nicknames to context information
-->
<p><code>NamedContext</code> 将昵称与上下文信息关联起来.</p>


<table class="table">
<thead><tr><th width="30%"><!--Field-->字段</th><th><!--Description-->描述</th></tr></thead>
<tbody>
    
  
<tr><td><code>name</code><B></br><!--[Required]-->[必需]</B><br/>
<code>string</code>
</td>
<td>
  <!--
  Name is the nickname for this Context
  -->
   <p><code>Name</code> 是该上下文的昵称</p>
</td>
</tr>
<tr><td><code>context</code><br/><B><!--[Required]-->[必需]</B>
<a href="#Context"><code>Context</code></a>
</td>
<td>
  <!---
  Context holds the context information
  -->
   <p><code>Context</code> 保存了上下文信息</p>
</td>
</tr>
</tbody>
</table>

## `NamedExtension`     {#NamedExtension}
    
<!--
**Appears in:**
-->
**出现在:**

- [Config](#Config)

- [AuthInfo](#AuthInfo)

- [Cluster](#Cluster)

- [Context](#Context)

- [Preferences](#Preferences)

<!---
NamedExtension relates nicknames to extension information.
-->
<p>NamedExtension 将昵称与扩展信息关联起来</p>


<table class="table">
<thead><tr><th width="30%"><!--Field-->字段</th><th><!--Description-->描述</th></tr></thead>
<tbody>
    
  
<tr><td><code>name</code><B><!--[Required]-->[必需]</B><br/>
<code>string</code>
</td>
<td>
  <!--
  Name is the nickname for this Extension
  --->
   <p><code>Name</code> 是该扩展的昵称.</p>
</td>
</tr>
<tr><td><code>extension</code><!--[Required]--><B>[必需]</B><br/>
<a href="https://pkg.go.dev/k8s.io/apimachinery/pkg/runtime/#RawExtension"><code>k8s.io/apimachinery/pkg/runtime.RawExtension</code></a>
</td>
<td>
  <!---
  Extension holds the extension information
  --->
   <p><code>Extension</code> 保存了扩展信息.</p>
</td>
</tr>
</tbody>
</table>

## `Preferences`     {#Preferences}
    
<!--
**Appears in:**
-->
**出现在:**

- [Config](#Config)



<table class="table">
<thead><tr><th width="30%"><!--Field-->字段</th><th><!--Description-->描述</th></tr></thead>
<tbody>
    
  
<tr><td><code>colors</code><br/>
<code>bool</code>
</td>
<td>
   <span class="text-muted">环境变量名称.</span></td>
</tr>
<tr><td><code>extensions</code><br/>
<a href="#NamedExtension"><code>[]NamedExtension</code></a>
</td>
<td>
  <!--
  Extensions holds additional information. This is useful for extenders so that reads and writes don't clobber unknown fields
  --->
   <p><code>Extensions</code> 保存额外信息. 这对于扩展器是有用的，这样读写不会破解未知字段.</p>
</td>
</tr>
</tbody>
</table>
