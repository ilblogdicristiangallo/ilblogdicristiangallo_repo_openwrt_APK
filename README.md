<h1>OpenWrt APK Repository by ilblogdicristiangallo OpenWrt 25.12.0 ></h1>

<div align="center">
  <img src="https://github.com/ilblogdicristiangallo/ilblogdicristiangallo_repo_openwrt_APK/blob/main/repository-openwrt-by-ilblogdicristiangallo.png?raw=true" 
       alt="Repository OpenWrt by ilblogdicristiangallo"
       width="600"
       style="height: auto;">
</div>

<h2>Access your router via SSH</h2>

<p>Connect to your OpenWrt router using PuTTY or any SSH client:</p>

<pre>ssh root@192.168.1.1</pre>

<p>Enter your password if required.</p>

<hr>

<h2>Add the ilblogdicristiangallo APK repository</h2>

<p>Append the repository URL to the APK sources list:</p>

<pre>echo "https://ilblogdicristiangallo.github.io/ilblogdicristiangallo_repo_openwrt_APK" >> /etc/apk/repositories</pre>

<p>Update the package index:</p>

<pre>apk update</pre>

<hr>

<h2>Import the repository public key</h2>

<p>Download the public key into the APK key directory:</p>

<pre>wget -O /etc/apk/keys/ilblogdicristiangallo.apkpub.pem \
https://github.com/ilblogdicristiangallo/ilblogdicristiangallo_repo_openwrt_APK/raw/main/ilblogdicristiangallo.apkpub.pem</pre>

<p>Verify that the key has been installed:</p>

<pre>ls /etc/apk/keys</pre>

<p>You should see:</p>

<pre>ilblogdicristiangallo.apkpub.pem</pre>

<hr>

<h2>Install packages from the repository</h2>

<p>Example:</p>

<pre>apk add telegramwrt</pre>

<hr>

<h2>Notes</h2>

<ul>
  <li>This repository is compatible <strong>only with OpenWrt 25.x</strong> (APK package manager).</li>
  <li>It does <strong>not</strong> work on OpenWrt 23.x or older (OPKG).</li>
  <li>Each package must include a valid <code>APKINDEX.tar.gz</code> file.</li>
  <li>The public key must be placed in <code>/etc/apk/keys/</code> for trusted installation.</li>
</ul>




