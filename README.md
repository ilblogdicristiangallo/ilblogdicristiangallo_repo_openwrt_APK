<h1>OpenWrt APK Repository by ilblogdicristiangallo OpenWrt 25.12.x</h1>

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
      <td>luci-app-apnweb</td>
      <td>1.0.5</td>
      <td>European APN Configurator with multi-language support (IT/EN), 37+ countries database with MNO and MVNO operators. Supports QMI, MBIM and ModemManager.</td>
    </tr>
    <tr>
      <td>telegramWrt</td>
      <td>1.0.7</td>
      <td>Modular Telegram bot for OpenWrt diagnostics and automation</td>
    </tr>
    <tr>
      <td>luci-app-teliasetup</td>
      <td>1.0.0</td>
      <td>LuCI app for ZTE MF286D that manages sequential FOTA firmware updates. Automatically detects the current version (B02-B12) and applies only the required updates. Bilingual web interface (IT/EN) with progress bar and live log.</td>
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

<pre>echo 'https://raw.githubusercontent.com/ilblogdicristiangallo/ilblogdicristiangallo_repo_openwrt_APK/main/packages.adb' >> /etc/apk/repositories.d/ilblogdicristiangallo.list</pre>

<p><strong>Step 2:</strong> Download and install the repository public key:</p>

<pre>wget https://raw.githubusercontent.com/ilblogdicristiangallo/ilblogdicristiangallo_repo_openwrt_APK/main/ilblogdicristiangallo.apkpub.pem \
     -O /etc/apk/keys/ilblogdicristiangallo.apkpub.pem</pre>

<p><strong>Step 3:</strong> Update the package index:</p>

<pre>apk update</pre>

<p><strong>Step 4:</strong> Install packages:</p>

<pre># Install LuCI APN Web Interface (European Configurator)
apk add luci-app-apnweb

# Install TelegramWrt Bot
apk add telegramWrt</pre>

<hr>

<h3>Method 2 — Direct Installation (No repository needed)</h3>

<p>This method installs the package directly from the file,
without adding the repository permanently.
Useful for quick tests or offline installations.</p>

<p><strong>Install luci-app-apnweb:</strong></p>

<pre>wget https://raw.githubusercontent.com/ilblogdicristiangallo/ilblogdicristiangallo_repo_openwrt_APK/main/luci-app-apnweb-1.0.5-r1.apk \
     -O /tmp/luci-app-apnweb.apk
apk add --allow-untrusted /tmp/luci-app-apnweb.apk</pre>

<p><strong>Install telegramWrt:</strong></p>

<pre>wget https://raw.githubusercontent.com/ilblogdicristiangallo/ilblogdicristiangallo_repo_openwrt_APK/main/telegramWrt-1.0.7-r1.apk \
     -O /tmp/telegramWrt.apk
apk add --allow-untrusted /tmp/telegramWrt.apk</pre>

<hr>

<h2>🖥️ luci-app-apnweb — European APN Configurator</h2>

<p>After installation, the APN configuration page is accessible directly
from the OpenWrt LuCI menu:</p>

<pre>Network → APN Configuration</pre>

<h3>✨ Main Features</h3>
<ul>
  <li>🌍 <strong>37+ European countries</strong> with country flags</li>
  <li>📡 <strong>MNO + MVNO operators</strong> database (main and virtual operators)</li>
  <li>🌐 <strong>Multi-language</strong> interface (Italian / English)</li>
  <li>⚡ <strong>Auto-fill</strong> APN, IP type, authentication, username and password</li>
  <li>📶 <strong>Hotspot APN</strong> separate configuration</li>
  <li>🔄 <strong>WAN restart</strong> and router reboot from interface</li>
  <li>🔐 <strong>SIM PIN</strong> management</li>
</ul>

<h3>🔌 Supported Connection Modes</h3>
<ul>
  <li>✅ <strong>QMI</strong> — Qualcomm MSM Interface</li>
  <li>✅ <strong>MBIM</strong> — Mobile Broadband Interface Model</li>
  <li>✅ <strong>ModemManager</strong> — Universal modem management (with 2G/3G/4G/5G selection)</li>
</ul>

<h3>🇪🇺 Supported Countries</h3>
<p>Italy 🇮🇹 • France 🇫🇷 • Germany 🇩🇪 • Spain 🇪🇸 • Portugal 🇵🇹 • 
United Kingdom 🇬🇧 • Ireland 🇮🇪 • Netherlands 🇳🇱 • Belgium 🇧🇪 • 
Luxembourg 🇱🇺 • Switzerland 🇨🇭 • Austria 🇦🇹 • Denmark 🇩🇰 • 
Sweden 🇸🇪 • Norway 🇳🇴 • Finland 🇫🇮 • Poland 🇵🇱 • Czech Republic 🇨🇿 • 
Slovakia 🇸🇰 • Hungary 🇭🇺 • Romania 🇷🇴 • Bulgaria 🇧🇬 • Croatia 🇭🇷 • 
Slovenia 🇸🇮 • Greece 🇬🇷 • Cyprus 🇨🇾 • Malta 🇲🇹 • Estonia 🇪🇪 • 
Latvia 🇱🇻 • Lithuania 🇱🇹 • Albania 🇦🇱 • Serbia 🇷🇸 • 
Bosnia and Herzegovina 🇧🇦 • Montenegro 🇲🇪 • North Macedonia 🇲🇰 • 
Moldova 🇲🇩 • Ukraine 🇺🇦</p>

<h3>📋 User Flow</h3>
<ol>
  <li>Select language (🇮🇹 Italiano / 🇬🇧 English)</li>
  <li>Select connection mode (QMI / MODEMMANAGER / MBIM)</li>
  <li>Select country from European list</li>
  <li>Select operator (filter MNO / MVNO / All)</li>
  <li>APN settings auto-filled — review and apply</li>
</ol>

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
  <li>After installation, refresh LuCI with <strong>Ctrl + F5</strong> to see the menu entry.</li>
</ul>

<hr>

<h2>📜 Changelog</h2>

<h3>luci-app-apnweb 1.0.5</h3>
<ul>
  <li>🆕 Complete redesign: European APN Configurator</li>
  <li>🆕 Multi-language interface (IT/EN) with language-first selection</li>
  <li>🆕 37+ European countries with flags</li>
  <li>🆕 MNO + MVNO operators database with filters</li>
  <li>🆕 Auto-fill APN, authentication, IP type, username, password</li>
  <li>🆕 Separate hotspot/tethering APN field</li>
  <li>🆕 External database (apn-database.js) for easy updates</li>
  <li>🔧 Improved compact UI</li>
</ul>

<h3>luci-app-apnweb 1.0.4</h3>
<ul>
  <li>Initial LuCI menu integration</li>
  <li>Support for QMI, MBIM, ModemManager</li>
  <li>Italian operators list</li>
</ul>

<hr>

<div align="center">
  <p>Made with ❤️ by 
    <a href="https://www.ilblogdicristiangallo.com">ilblogdicristiangallo</a>
  </p>
</div>
