<h1>OpenWrt APK Repository by ilblogdicristiangallo OpenWrt 25.12.0 ></h1>

<div align="center">
  <img src="https://github.com/ilblogdicristiangallo/ilblogdicristiangallo_repo_openwrt_APK/blob/main/repository-openwrt-by-ilblogdicristiangallo.png?raw=true" 
       alt="Repository OpenWrt by ilblogdicristiangallo"
       width="600"
       style="height: auto;">
</div>

<div align="center">
  <p>Custom APK packages for OpenWrt 25.x</p>
</div>

<hr>

<h2>⚠️ Compatibility</h2>

<ul>
  <li>✅ Compatible with <strong>OpenWrt 25.x</strong> (APK package manager)</li>
  <li>❌ Does <strong>NOT</strong> work on OpenWrt 23.x or older (OPKG)</li>
</ul>

<hr>

<h2>📦 Available Packages</h2>

<table>
  <thead>
    <tr>
      <th>Package</th>
      <th>Version</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>apn-web</td>
      <td>1.0.3</td>
      <td>Simple web interface for APN configuration</td>
    </tr>
    <tr>
      <td>telegramWrt</td>
      <td>1.0.7</td>
      <td>Modular Telegram bot for OpenWrt diagnostics and automation</td>
    </tr>
  </tbody>
</table>

<hr>

<h2>🔧 Installation</h2>

<h3>Access your router via SSH</h3>

<p>Connect to your OpenWrt router using PuTTY or any SSH client:</p>

<pre>ssh root@192.168.1.1</pre>

<p>Enter your password if required.</p>

<hr>

<h3>Method 1 — Install from Repository (Recommended)</h3>

<p>This method adds the repository permanently to your router.
Packages can be updated anytime with <code>apk update</code>.</p>

<p><strong>Step 1:</strong> Add the repository to the APK sources list:</p>

<pre>echo 'https://ilblogdicristiangallo.github.io/ilblogdicristiangallo_repo_openwrt_APK/packages.adb' >> /etc/apk/repositories.d/customfeeds.list</pre>

<p><strong>Step 2:</strong> Download and install the repository public key:</p>

<pre>wget https://github.com/ilblogdicristiangallo/ilblogdicristiangallo_repo_openwrt_APK/raw/main/ilblogdicristiangallo.apkpub.pem \
     -O /etc/apk/keys/ilblogdicristiangallo.apkpub.pem</pre>

<p><strong>Step 3:</strong> Update the package index:</p>

<pre>apk update</pre>

<p><strong>Step 4:</strong> Install packages:</p>

<pre># Install APN Web Interface
apk add apn-web

# Install TelegramWrt Bot
apk add telegramWrt</pre>

<hr>

<h3>Method 2 — Direct Installation (No repository needed)</h3>

<p>This method installs the package directly from the file,
without adding the repository permanently.
Useful for quick tests or offline installations.</p>

<p><strong>Install apn-web:</strong></p>

<pre>wget https://github.com/ilblogdicristiangallo/ilblogdicristiangallo_repo_openwrt_APK/raw/main/apn-web-1.0.3-r1.apk \
     -O /tmp/apn-web.apk
apk add --allow-untrusted /tmp/apn-web.apk</pre>

<p><strong>Install telegramWrt:</strong></p>

<pre>wget https://github.com/ilblogdicristiangallo/ilblogdicristiangallo_repo_openwrt_APK/raw/main/telegramWrt-1.0.7-r1.apk \
     -O /tmp/telegramWrt.apk
apk add --allow-untrusted /tmp/telegramWrt.apk</pre>

<hr>

<h2>🔑 About the Public Key</h2>

<p>The public key is required only for <strong>Method 1</strong>
to verify the authenticity of the packages.</p>

<p>Verify that the key has been installed correctly:</p>

<pre>ls /etc/apk/keys/</pre>

<p>You should see:</p>

<pre>ilblogdicristiangallo.apkpub.pem</pre>

<hr>

<h2>📝 Notes</h2>

<ul>
  <li>This repository is compatible <strong>only with OpenWrt 25.x</strong>.</li>
  <li>It does <strong>NOT</strong> work on OpenWrt 23.x or older (OPKG).</li>
  <li>For <strong>Method 1</strong>, the public key must be placed in
      <code>/etc/apk/keys/</code> for trusted installation.</li>
  <li>For <strong>Method 2</strong>, no key is needed but the flag
      <code>--allow-untrusted</code> is required.</li>
  <li>The repository index is based on <code>packages.adb</code> format,
      compatible with OpenWrt 25.x APK tools.</li>
</ul>

<hr>

<div align="center">
  <p>Made with ❤️ by 
    <a href="https://github.com/ilblogdicristiangallo">ilblogdicristiangallo</a>
  </p>
</div>




