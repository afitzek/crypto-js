<p>Copied the documentation from: https://code.google.com/p/crypto-js/</p>
<p>According to: https://code.google.com/p/crypto-js/ the code is liscensed under: New BSD License: </p>
<p>
  (c) 2009-2013 by Jeff Mott. All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

Redistributions of source code must retain the above copyright notice, this list of conditions, and the following disclaimer.
Redistributions in binary form must reproduce the above copyright notice, this list of conditions, and the following disclaimer in the documentation or other materials provided with the distribution.
Neither the name CryptoJS nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS," AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE, ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
</p>

<hr>
<h2>Now the real documentation:</h2>
<hr>

<p>CryptoJS is a growing collection of standard and secure cryptographic algorithms implemented in JavaScript using best practices and patterns. They are fast, and they have a consistent and simple interface. </p><p>If you have a problem with CryptoJS, if you want to discuss new features, or if you want to contribute to the project, you can visit the CryptoJS discussion group. </p><p><a href="http://groups.google.com/group/crypto-js/topics" rel="nofollow">http://groups.google.com/group/crypto-js/topics</a> </p><hr/><h1><a name="Inactivity"></a>Inactivity<a href="#Inactivity" class="section_anchor"></a></h1><p>CryptoJS is a project that I enjoy and work on in my spare time, but unfortunately my 9-to-5 hasn&#x27;t left me with as much free time as it used to. I&#x27;d still like to continue improving it in the future, but I can&#x27;t say when that will be. If you find that CryptoJS doesn&#x27;t meet your needs, then I&#x27;d recommend you try <a href="https://github.com/digitalbazaar/forge" rel="nofollow">Forge</a>. </p><hr/><h1><a name="CryptoJS_3.1"></a>CryptoJS 3.1<a href="#CryptoJS_3.1" class="section_anchor"></a></h1><ul><li>SHA-3! </li><li>RIPEMD-160 </li><li>Typed arrays </li></ul><p>See the full <a href="/p/crypto-js/wiki/ChangeLog">ChangeLog</a>. </p><hr/><p><ul><li><a href="#Inactivity">Inactivity</a></li><li><a href="#CryptoJS_3.1">CryptoJS 3.1</a></li><li><a href="#Quick-start_Guide">Quick-start Guide</a></li><ul><li><a href="#Hashers">Hashers</a></li><ul><li><a href="#The_Hasher_Algorithms">The Hasher Algorithms</a></li><ul><li><a href="#MD5">MD5</a></li><li><a href="#SHA-1">SHA-1</a></li><li><a href="#SHA-2">SHA-2</a></li><li><a href="#SHA-3">SHA-3</a></li><li><a href="#RIPEMD-160">RIPEMD-160</a></li></ul><li><a href="#The_Hasher_Input">The Hasher Input</a></li><li><a href="#The_Hasher_Output">The Hasher Output</a></li><li><a href="#Progressive_Hashing">Progressive Hashing</a></li></ul><li><a href="#HMAC">HMAC</a></li><ul><li><a href="#Progressive_HMAC_Hashing">Progressive HMAC Hashing</a></li></ul><li><a href="#PBKDF2">PBKDF2</a></li><li><a href="#Ciphers">Ciphers</a></li><ul><li><a href="#The_Cipher_Algorithms">The Cipher Algorithms</a></li><ul><li><a href="#AES">AES</a></li><li><a href="#DES,_Triple_DES">DES, Triple DES</a></li><li><a href="#Rabbit">Rabbit</a></li><li><a href="#RC4,_RC4Drop">RC4, RC4Drop</a></li></ul><li><a href="#Custom_Key_and_IV">Custom Key and IV</a></li><li><a href="#Block_Modes_and_Padding">Block Modes and Padding</a></li><li><a href="#The_Cipher_Input">The Cipher Input</a></li><li><a href="#The_Cipher_Output">The Cipher Output</a></li><li><a href="#Progressive_Ciphering">Progressive Ciphering</a></li><li><a href="#Interoperability">Interoperability</a></li><ul><li><a href="#With_OpenSSL">With OpenSSL</a></li></ul></ul><li><a href="#Encoders">Encoders</a></li></ul></ul> </p><hr/><h1><a name="Quick-start_Guide"></a>Quick-start Guide<a href="#Quick-start_Guide" class="section_anchor"></a></h1><h2><a name="Hashers"></a>Hashers<a href="#Hashers" class="section_anchor"></a></h2><h3><a name="The_Hasher_Algorithms"></a>The Hasher Algorithms<a href="#The_Hasher_Algorithms" class="section_anchor"></a></h3><h4><a name="MD5"></a>MD5<a href="#MD5" class="section_anchor"></a></h4><p>MD5 is a widely used hash function. It&#x27;s been used in a variety of security applications and is also commonly used to check the integrity of files. Though, MD5 is not collision resistant, and it isn&#x27;t suitable for applications like SSL certificates or digital signatures that rely on this property. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/md5.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var hash = CryptoJS.MD5(&quot;Message&quot;);
&lt;/script&gt;</pre><h4><a name="SHA-1"></a>SHA-1<a href="#SHA-1" class="section_anchor"></a></h4><p>The SHA hash functions were designed by the National Security Agency (NSA). SHA-1 is the most established of the existing SHA hash functions, and it&#x27;s used in a variety of security applications and protocols. Though, SHA-1&#x27;s collision resistance has been weakening as new attacks are discovered or improved. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/sha1.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var hash = CryptoJS.SHA1(&quot;Message&quot;);
&lt;/script&gt;</pre><h4><a name="SHA-2"></a>SHA-2<a href="#SHA-2" class="section_anchor"></a></h4><p>SHA-256 is one of the four variants in the SHA-2 set. It isn&#x27;t as widely used as SHA-1, though it appears to provide much better security. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/sha256.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var hash = CryptoJS.SHA256(&quot;Message&quot;);
&lt;/script&gt;</pre><p>SHA-512 is largely identical to SHA-256 but operates on 64-bit words rather than 32. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/sha512.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var hash = CryptoJS.SHA512(&quot;Message&quot;);
&lt;/script&gt;</pre><p>CryptoJS also supports SHA-224 and SHA-384, which are largely identical but truncated versions of SHA-256 and SHA-512 respectively. </p><h4><a name="SHA-3"></a>SHA-3<a href="#SHA-3" class="section_anchor"></a></h4><p>SHA-3 is the winner of a five-year competition to select a new cryptographic hash algorithm where 64 competing designs were evaluated. </p><p><strong>NOTE:</strong> I made a mistake when I named this implementation SHA-3. It should be named Keccak[c=2d]. Each of the SHA-3 functions is based on an instance of the Keccak algorithm, which NIST selected as the winner of the SHA-3 competition, but those SHA-3 functions won&#x27;t produce hashes identical to Keccak. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/sha3.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var hash = CryptoJS.SHA3(&quot;Message&quot;);
&lt;/script&gt;</pre><p>SHA-3 can be configured to output hash lengths of one of 224, 256, 384, or 512 bits. The default is 512 bits. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/sha3.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var hash = CryptoJS.SHA3(&quot;Message&quot;, { outputLength: 512 });
    var hash = CryptoJS.SHA3(&quot;Message&quot;, { outputLength: 384 });
    var hash = CryptoJS.SHA3(&quot;Message&quot;, { outputLength: 256 });
    var hash = CryptoJS.SHA3(&quot;Message&quot;, { outputLength: 224 });
&lt;/script&gt;</pre><h4><a name="RIPEMD-160"></a>RIPEMD-160<a href="#RIPEMD-160" class="section_anchor"></a></h4><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/ripemd160.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var hash = CryptoJS.RIPEMD160(&quot;Message&quot;);
&lt;/script&gt;</pre><h3><a name="The_Hasher_Input"></a>The Hasher Input<a href="#The_Hasher_Input" class="section_anchor"></a></h3><p>The hash algorithms accept either strings or instances of CryptoJS.lib.WordArray. A WordArray object represents an array of 32-bit words. When you pass a string, it&#x27;s automatically converted to a WordArray encoded as UTF-8. </p><h3><a name="The_Hasher_Output"></a>The Hasher Output<a href="#The_Hasher_Output" class="section_anchor"></a></h3><p>The hash you get back isn&#x27;t a string yet. It&#x27;s a WordArray object. When you use a WordArray object in a string context, it&#x27;s automatically converted to a hex string. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/sha256.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var hash = CryptoJS.SHA256(&quot;Message&quot;);

    alert(typeof hash); // object

    alert(hash); // 2f77668a9dfbf8d5848b9eeb4a7145ca94c6ed9236e4a773f6dcafa5132b2f91
&lt;/script&gt;</pre><p>You can convert a WordArray object to other formats by explicitly calling the toString method and passing an encoder. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/sha256.js&quot;&gt;&lt;/script&gt;
&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/components/enc-base64-min.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var hash = CryptoJS.SHA256(&quot;Message&quot;);

    alert(hash.toString(CryptoJS.enc.Base64)); // L3dmip37+NWEi57rSnFFypTG7ZI25Kdz9tyvpRMrL5E=

    alert(hash.toString(CryptoJS.enc.Latin1)); // /wf��ûøÕ���ëJqEÊ�Æí�6ä§söÜ¯¥+/�

    alert(hash.toString(CryptoJS.enc.Hex)); // 2f77668a9dfbf8d5848b9eeb4a7145ca94c6ed9236e4a773f6dcafa5132b2f91
&lt;/script&gt;</pre><h3><a name="Progressive_Hashing"></a>Progressive Hashing<a href="#Progressive_Hashing" class="section_anchor"></a></h3><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/sha256.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var sha256 = CryptoJS.algo.SHA256.create();

    sha256.update(&quot;Message Part 1&quot;);
    sha256.update(&quot;Message Part 2&quot;);
    sha256.update(&quot;Message Part 3&quot;);

    var hash = sha256.finalize();
&lt;/script&gt;</pre><h2><a name="HMAC"></a>HMAC<a href="#HMAC" class="section_anchor"></a></h2><p>Keyed-hash message authentication codes (HMAC) is a mechanism for message authentication using cryptographic hash functions. </p><p>HMAC can be used in combination with any iterated cryptographic hash function. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/hmac-md5.js&quot;&gt;&lt;/script&gt;
&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/hmac-sha1.js&quot;&gt;&lt;/script&gt;
&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/hmac-sha256.js&quot;&gt;&lt;/script&gt;
&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/hmac-sha512.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var hash = CryptoJS.HmacMD5(&quot;Message&quot;, &quot;Secret Passphrase&quot;);
    var hash = CryptoJS.HmacSHA1(&quot;Message&quot;, &quot;Secret Passphrase&quot;);
    var hash = CryptoJS.HmacSHA256(&quot;Message&quot;, &quot;Secret Passphrase&quot;);
    var hash = CryptoJS.HmacSHA512(&quot;Message&quot;, &quot;Secret Passphrase&quot;);
&lt;/script&gt;</pre><h3><a name="Progressive_HMAC_Hashing"></a>Progressive HMAC Hashing<a href="#Progressive_HMAC_Hashing" class="section_anchor"></a></h3><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/hmac-sha256.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var hmac = CryptoJS.algo.HMAC.create(CryptoJS.algo.SHA256, &quot;Secret Passphrase&quot;);

    hmac.update(&quot;Message Part 1&quot;);
    hmac.update(&quot;Message Part 2&quot;);
    hmac.update(&quot;Message Part 3&quot;);

    var hash = hmac.finalize();
&lt;/script&gt;</pre><h2><a name="PBKDF2"></a>PBKDF2<a href="#PBKDF2" class="section_anchor"></a></h2><p>PBKDF2 is a password-based key derivation function. In many applications of cryptography, user security is ultimately dependent on a password, and because a password usually can&#x27;t be used directly as a cryptographic key, some processing is required. </p><p>A salt provides a large set of keys for any given password, and an iteration count increases the cost of producing keys from a password, thereby also increasing the difficulty of attack. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/pbkdf2.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var salt = CryptoJS.lib.WordArray.random(128/8);

    var key128Bits = CryptoJS.PBKDF2(&quot;Secret Passphrase&quot;, salt, { keySize: 128/32 });
    var key256Bits = CryptoJS.PBKDF2(&quot;Secret Passphrase&quot;, salt, { keySize: 256/32 });
    var key512Bits = CryptoJS.PBKDF2(&quot;Secret Passphrase&quot;, salt, { keySize: 512/32 });

    var key512Bits1000Iterations = CryptoJS.PBKDF2(&quot;Secret Passphrase&quot;, salt, { keySize: 512/32, iterations: 1000 });
&lt;/script&gt;</pre><h2><a name="Ciphers"></a>Ciphers<a href="#Ciphers" class="section_anchor"></a></h2><h3><a name="The_Cipher_Algorithms"></a>The Cipher Algorithms<a href="#The_Cipher_Algorithms" class="section_anchor"></a></h3><h4><a name="AES"></a>AES<a href="#AES" class="section_anchor"></a></h4><p>The Advanced Encryption Standard (AES) is a U.S. Federal Information Processing Standard (FIPS). It was selected after a 5-year process where 15 competing designs were evaluated. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/aes.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var encrypted = CryptoJS.AES.encrypt(&quot;Message&quot;, &quot;Secret Passphrase&quot;);

    var decrypted = CryptoJS.AES.decrypt(encrypted, &quot;Secret Passphrase&quot;);
&lt;/script&gt;</pre><p>CryptoJS supports AES-128, AES-192, and AES-256. It will pick the variant by the size of the key you pass in. If you use a passphrase, then it will generate a 256-bit key. </p><h4><a name="DES,_Triple_DES"></a>DES, Triple DES<a href="#DES,_Triple_DES" class="section_anchor"></a></h4><p>DES is a previously dominant algorithm for encryption, and was published as an official Federal Information Processing Standard (FIPS). DES is now considered to be insecure due to the small key size. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/tripledes.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var encrypted = CryptoJS.DES.encrypt(&quot;Message&quot;, &quot;Secret Passphrase&quot;);

    var decrypted = CryptoJS.DES.decrypt(encrypted, &quot;Secret Passphrase&quot;);
&lt;/script&gt;</pre><p>Triple DES applies DES three times to each block to increase the key size. The algorithm is believed to be secure in this form. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/tripledes.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var encrypted = CryptoJS.TripleDES.encrypt(&quot;Message&quot;, &quot;Secret Passphrase&quot;);

    var decrypted = CryptoJS.TripleDES.decrypt(encrypted, &quot;Secret Passphrase&quot;);
&lt;/script&gt;</pre><h4><a name="Rabbit"></a>Rabbit<a href="#Rabbit" class="section_anchor"></a></h4><p>Rabbit is a high-performance stream cipher and a finalist in the eSTREAM Portfolio. It is one of the four designs selected after a 3 1/2-year process where 22 designs were evaluated. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/rabbit.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var encrypted = CryptoJS.Rabbit.encrypt(&quot;Message&quot;, &quot;Secret Passphrase&quot;);

    var decrypted = CryptoJS.Rabbit.decrypt(encrypted, &quot;Secret Passphrase&quot;);
&lt;/script&gt;</pre><h4><a name="RC4,_RC4Drop"></a>RC4, RC4Drop<a href="#RC4,_RC4Drop" class="section_anchor"></a></h4><p>RC4 is a widely-used stream cipher. It&#x27;s used in popular protocols such as SSL and WEP. Although remarkable for its simplicity and speed, the algorithm&#x27;s history doesn&#x27;t inspire confidence in its security. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/rc4.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var encrypted = CryptoJS.RC4.encrypt(&quot;Message&quot;, &quot;Secret Passphrase&quot;);

    var decrypted = CryptoJS.RC4.decrypt(encrypted, &quot;Secret Passphrase&quot;);
&lt;/script&gt;</pre><p>It was discovered that the first few bytes of keystream are strongly non-random and leak information about the key. We can defend against this attack by discarding the initial portion of the keystream. This modified algorithm is traditionally called RC4-drop. </p><p>By default, 192 words (768 bytes) are dropped, but you can configure the algorithm to drop any number of words. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/rc4.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var encrypted = CryptoJS.RC4Drop.encrypt(&quot;Message&quot;, &quot;Secret Passphrase&quot;);

    var encrypted = CryptoJS.RC4Drop.encrypt(&quot;Message&quot;, &quot;Secret Passphrase&quot;, { drop: 3072/4 });

    var decrypted = CryptoJS.RC4Drop.decrypt(encrypted, &quot;Secret Passphrase&quot;, { drop: 3072/4 });
&lt;/script&gt;</pre><h3><a name="Custom_Key_and_IV"></a>Custom Key and IV<a href="#Custom_Key_and_IV" class="section_anchor"></a></h3><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/aes.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var key = CryptoJS.enc.Hex.parse(&#x27;000102030405060708090a0b0c0d0e0f&#x27;);
    var iv  = CryptoJS.enc.Hex.parse(&#x27;101112131415161718191a1b1c1d1e1f&#x27;);

    var encrypted = CryptoJS.AES.encrypt(&quot;Message&quot;, key, { iv: iv });
&lt;/script&gt;</pre><h3><a name="Block_Modes_and_Padding"></a>Block Modes and Padding<a href="#Block_Modes_and_Padding" class="section_anchor"></a></h3><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/aes.js&quot;&gt;&lt;/script&gt;
&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/components/mode-cfb-min.js&quot;&gt;&lt;/script&gt;
&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/components/pad-ansix923-min.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var encrypted = CryptoJS.AES.encrypt(&quot;Message&quot;, &quot;Secret Passphrase&quot;, { mode: CryptoJS.mode.CFB, padding: CryptoJS.pad.AnsiX923 });
&lt;/script&gt;</pre><p>CryptoJS supports the following modes: </p><ul><li>CBC (the default) </li><li>CFB </li><li>CTR </li><li>OFB </li><li>ECB </li></ul><p>And CryptoJS supports the following padding schemes: </p><ul><li>Pkcs7 (the default) </li><li>Iso97971 </li><li>AnsiX923 </li><li>Iso10126 </li><li>ZeroPadding </li><li>NoPadding </li></ul><h3><a name="The_Cipher_Input"></a>The Cipher Input<a href="#The_Cipher_Input" class="section_anchor"></a></h3><p>For the plaintext message, the cipher algorithms accept either strings or instances of CryptoJS.lib.WordArray. </p><p>For the key, when you pass a string, it&#x27;s treated as a passphrase and used to derive an actual key and IV. Or you can pass a WordArray that represents the actual key. If you pass the actual key, you must also pass the actual IV. </p><p>For the ciphertext, the cipher algorithms accept either strings or instances of CryptoJS.lib.CipherParams. A CipherParams object represents a collection of parameters such as the IV, a salt, and the raw ciphertext itself. When you pass a string, it&#x27;s automatically converted to a CipherParams object according to a configurable format strategy. </p><h3><a name="The_Cipher_Output"></a>The Cipher Output<a href="#The_Cipher_Output" class="section_anchor"></a></h3><p>The plaintext you get back after decryption is a WordArray object. See Hashers&#x27; Output for more detail. </p><p>The ciphertext you get back after encryption isn&#x27;t a string yet. It&#x27;s a CipherParams object. A CipherParams object gives you access to all the parameters used during encryption. When you use a CipherParams object in a string context, it&#x27;s automatically converted to a string according to a format strategy. The default is an OpenSSL-compatible format. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/aes.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var encrypted = CryptoJS.AES.encrypt(&quot;Message&quot;, &quot;Secret Passphrase&quot;);

    alert(encrypted.key);        // 74eb593087a982e2a6f5dded54ecd96d1fd0f3d44a58728cdcd40c55227522223
    alert(encrypted.iv);         // 7781157e2629b094f0e3dd48c4d786115
    alert(encrypted.salt);       // 7a25f9132ec6a8b34
    alert(encrypted.ciphertext); // 73e54154a15d1beeb509d9e12f1e462a0

    alert(encrypted);            // U2FsdGVkX1+iX5Ey7GqLND5UFUoV0b7rUJ2eEvHkYqA=
&lt;/script&gt;</pre><p>You can define your own formats in order to be compatible with other crypto implementations. A format is an object with two methods—stringify and parse—that converts between CipherParams objects and ciphertext strings. </p><p>Here&#x27;s how you might write a JSON formatter: </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/aes.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var JsonFormatter = {
        stringify: function (cipherParams) {
            // create json object with ciphertext
            var jsonObj = {
                ct: cipherParams.ciphertext.toString(CryptoJS.enc.Base64)
            };

            // optionally add iv and salt
            if (cipherParams.iv) {
                jsonObj.iv = cipherParams.iv.toString();
            }
            if (cipherParams.salt) {
                jsonObj.s = cipherParams.salt.toString();
            }

            // stringify json object
            return JSON.stringify(jsonObj);
        },

        parse: function (jsonStr) {
            // parse json string
            var jsonObj = JSON.parse(jsonStr);

            // extract ciphertext from json object, and create cipher params object
            var cipherParams = CryptoJS.lib.CipherParams.create({
                ciphertext: CryptoJS.enc.Base64.parse(jsonObj.ct)
            });

            // optionally extract iv and salt
            if (jsonObj.iv) {
                cipherParams.iv = CryptoJS.enc.Hex.parse(jsonObj.iv)
            }
            if (jsonObj.s) {
                cipherParams.salt = CryptoJS.enc.Hex.parse(jsonObj.s)
            }

            return cipherParams;
        }
    };

    var encrypted = CryptoJS.AES.encrypt(&quot;Message&quot;, &quot;Secret Passphrase&quot;, { format: JsonFormatter });

    alert(encrypted); // {&quot;ct&quot;:&quot;tZ4MsEnfbcDOwqau68aOrQ==&quot;,&quot;iv&quot;:&quot;8a8c8fd8fe33743d3638737ea4a00698&quot;,&quot;s&quot;:&quot;ba06373c8f57179c&quot;}

    var decrypted = CryptoJS.AES.decrypt(encrypted, &quot;Secret Passphrase&quot;, { format: JsonFormatter });

    alert(decrypted.toString(CryptoJS.enc.Utf8)); // Message
&lt;/script&gt;</pre><h3><a name="Progressive_Ciphering"></a>Progressive Ciphering<a href="#Progressive_Ciphering" class="section_anchor"></a></h3><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/aes.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var key = CryptoJS.enc.Hex.parse(&#x27;000102030405060708090a0b0c0d0e0f&#x27;);
    var iv  = CryptoJS.enc.Hex.parse(&#x27;101112131415161718191a1b1c1d1e1f&#x27;);

    var aesEncryptor = CryptoJS.algo.AES.createEncryptor(key, { iv: iv });

    var ciphertextPart1 = aesEncryptor.process(&quot;Message Part 1&quot;);
    var ciphertextPart2 = aesEncryptor.process(&quot;Message Part 2&quot;);
    var ciphertextPart3 = aesEncryptor.process(&quot;Message Part 3&quot;);
    var ciphertextPart4 = aesEncryptor.finalize();

    var aesDecryptor = CryptoJS.algo.AES.createDecryptor(key, { iv: iv });

    var plaintextPart1 = aesDecryptor.process(ciphertextPart1);
    var plaintextPart2 = aesDecryptor.process(ciphertextPart2);
    var plaintextPart3 = aesDecryptor.process(ciphertextPart3);
    var plaintextPart4 = aesDecryptor.process(ciphertextPart4);
    var plaintextPart5 = aesDecryptor.finalize();
&lt;/script&gt;</pre><h3><a name="Interoperability"></a>Interoperability<a href="#Interoperability" class="section_anchor"></a></h3><h4><a name="With_OpenSSL"></a>With OpenSSL<a href="#With_OpenSSL" class="section_anchor"></a></h4><p>Encrypt with OpenSSL: </p><pre class="prettyprint">openssl enc -aes-256-cbc -in infile -out outfile -pass pass:&quot;Secret Passphrase&quot; -e -base64</pre><p>Decrypt with CryptoJS: </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/aes.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var decrypted = CryptoJS.AES.decrypt(openSSLEncrypted, &quot;Secret Passphrase&quot;);
&lt;/script&gt;</pre><h2><a name="Encoders"></a>Encoders<a href="#Encoders" class="section_anchor"></a></h2><p>CryptoJS can convert from encoding formats such as Base64, Latin1 or Hex to WordArray objects and vica versa. </p><pre class="prettyprint">&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/components/core-min.js&quot;&gt;&lt;/script&gt;
&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/components/enc-utf16-min.js&quot;&gt;&lt;/script&gt;
&lt;script src=&quot;http://crypto-js.googlecode.com/svn/tags/3.1.2/build/components/enc-base64-min.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    var words  = CryptoJS.enc.Base64.parse(&#x27;SGVsbG8sIFdvcmxkIQ==&#x27;);
    var base64 = CryptoJS.enc.Base64.stringify(words);

    var words  = CryptoJS.enc.Latin1.parse(&#x27;Hello, World!&#x27;);
    var latin1 = CryptoJS.enc.Latin1.stringify(words);

    var words = CryptoJS.enc.Hex.parse(&#x27;48656c6c6f2c20576f726c6421&#x27;);
    var hex   = CryptoJS.enc.Hex.stringify(words);

    var words = CryptoJS.enc.Utf8.parse(&#x27;𤭢&#x27;);
    var utf8  = CryptoJS.enc.Utf8.stringify(words);

    var words = CryptoJS.enc.Utf16.parse(&#x27;Hello, World!&#x27;);
    var utf16 = CryptoJS.enc.Utf16.stringify(words);

    var words = CryptoJS.enc.Utf16LE.parse(&#x27;Hello, World!&#x27;);
    var utf16 = CryptoJS.enc.Utf16LE.stringify(words);
&lt;/script&gt;</pre>
