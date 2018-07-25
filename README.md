# Run a Puppet module with no Master server

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Copyright Glen Buktenica](https://img.shields.io/badge/Copyright-Glen_Buktenica-blue.svg)](http://buktenica.com)

This is example code to run a Puppet manifest with out a Puppet Master (Masterless).

## Run repository

```bash
yum install puppet -y
git clone <THIS REPO>
cd Puppet_Masterless
/opt/puppetlabs/bin/puppet apply --modulepath ./modules manifests/site.pp
```

Expected output

```plaintext
Notice: /Stage[main]/Foo/File[/tmp/hello]/ensure: defined content as '{md5}3e25960a79dbc69b674cd4ec67a72c62'
Notice: Applied catalog in 0.11 seconds
```

## Testing

```bash
cat /tmp/hello
```

Expected output

```Plaintext
Hello world [root@hostname tmp]#
```