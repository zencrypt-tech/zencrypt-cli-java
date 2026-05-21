<!--
*****************************************************************************************
Title: Zencrypt CLI Java Readme **********************************************************
Developed by: Ryan Hatch / Zencrypt Tech *************************************************
Dev Date: Oct 26th 2022 ******************************************************************
Last Updated: 2026 ************************************************************************
Version: 2.0 ******************************************************************************
*****************************************************************************************
-->

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
  </head>
  <body>
    <br>

    <h1 align="center">Zencrypt CLI Java</h1>

    <p align="center">
      <strong>By: Ryan Hatch / Zencrypt Tech</strong>
      <br>
      <em>Keeping It Simple and Secure.</em>
    </p>

    <p align="center">
      <a href="#overview">Overview</a> •
      <a href="#features">Features</a> •
      <a href="#requirements">Requirements</a> •
      <a href="#installation">Installation</a> •
      <a href="#usage">Usage</a> •
      <a href="#cryptography-notes">Cryptography Notes</a> •
      <a href="#building-and-running">Build</a> •
      <a href="#contributing">Contributing</a> •
      <a href="#disclaimer">Disclaimer</a> •
      <a href="#license">License</a>
    </p>

    <hr>

    <p align="center">
      &copy; 2026 Ryan Hatch / Zencrypt Tech
      <br>
      All Rights Reserved.
    </p>

    <br>

    <h2 id="overview">Overview</h2>

    <p>
      Zencrypt CLI Java is a terminal-based encryption and hashing tool from the
      Zencrypt Tech project family.
    </p>

    <p>
      This CLI provides a simple local interface for generating and verifying
      SHA-256 hashes, encrypting and decrypting text, encrypting and decrypting
      files, copying output, and clearing clipboard content.
    </p>

    <p>
      This repository is the Java CLI version of Zencrypt. It is intended for
      learning, experimentation, and local encryption workflows while keeping the
      interface simple, direct, and command-line focused.
    </p>

    <hr>

    <h2 id="features">Features</h2>

    <ul>
      <li>
        <strong>Hash generation</strong> using the SHA-256 hashing algorithm with
        an optional salt value.
      </li>
      <li>
        <strong>Hash verification</strong> by comparing provided text and salt
        input against a known hash.
      </li>
      <li>
        <strong>Encrypt and decrypt text</strong> using AES symmetric encryption.
      </li>
      <li>
        <strong>Encrypt and decrypt files</strong> with AES-based file encryption.
      </li>
      <li>
        <strong>Copy output</strong> to the clipboard for easier terminal workflows.
      </li>
      <li>
        <strong>Clear content</strong> from the clipboard after sensitive operations.
      </li>
      <li>
        <strong>Local-first design</strong> for running encryption and hashing tasks
        directly from the user's machine.
      </li>
    </ul>

    <hr>

    <h2 id="requirements">Requirements</h2>

    <p>
      Java Development Kit 8+ is recommended.
    </p>

    <p>
      Confirm Java and the Java compiler are available from your terminal:
    </p>

    <pre><code>java -version
javac -version</code></pre>

    <p>
      Recommended tools:
    </p>

    <ul>
      <li>JDK 8 or newer</li>
      <li>Git</li>
      <li>Windows Command Prompt, PowerShell, macOS Terminal, or a Linux shell</li>
    </ul>

    <hr>

    <h2 id="installation">Installation</h2>

    <p>
      To install Zencrypt CLI Java, you will need Java and Git installed on your
      system.
    </p>

    <ol>
      <li>
        Clone the repository:
        <pre><code>git clone https://github.com/zencrypt-tech/zencrypt-cli-java.git</code></pre>
      </li>
      <li>
        Navigate into the project folder:
        <pre><code>cd zencrypt-cli-java</code></pre>
      </li>
      <li>
        Compile the Java source file:
        <pre><code>javac Zencrypt.java</code></pre>
      </li>
    </ol>

    <hr>

    <h2 id="usage">Usage</h2>

    <p>
      Run the application with:
    </p>

    <pre><code>java Zencrypt</code></pre>

    <p>
      Follow the on-screen prompts to perform the desired operation.
    </p>

    <h3>Main Menu</h3>

    <pre><code>1 | Hash Manager
2 | Encrypt Text
3 | Encrypt Files
4 | Clear Clipboard
5 | Exit</code></pre>

    <hr>

    <h2 id="hash-manager">Hash Manager</h2>

    <p>
      The Hash Manager provides SHA-256 hashing workflows for generating and
      checking hashes from the terminal.
    </p>

    <ul>
      <li>Enter text input.</li>
      <li>Add an optional salt value.</li>
      <li>Generate a SHA-256 hash.</li>
      <li>Compare generated output against a known hash value.</li>
    </ul>

    <p>
      SHA-256 is a one-way hashing algorithm. It is useful for checksums,
      fingerprints, verification exercises, and learning how fixed-length hash
      output works.
    </p>

    <hr>

    <h2 id="text-encryption">Text Encryption</h2>

    <p>
      The text encryption workflow allows users to encrypt and decrypt text
      directly from the terminal using AES symmetric encryption.
    </p>

    <ol>
      <li>Choose the text encryption option from the menu.</li>
      <li>Enter the plaintext message.</li>
      <li>Provide the required encryption input when prompted.</li>
      <li>Copy or save the encrypted output.</li>
      <li>Use the matching decryption workflow to restore the plaintext.</li>
    </ol>

    <hr>

    <h2 id="file-encryption">File Encryption</h2>

    <p>
      The file encryption workflow allows users to encrypt and decrypt local files
      from the command line.
    </p>

    <ol>
      <li>Choose the file encryption option from the menu.</li>
      <li>Enter the target file path.</li>
      <li>Provide the required encryption input when prompted.</li>
      <li>Save the encrypted file output.</li>
      <li>Use the matching decryption workflow to restore the file.</li>
    </ol>

    <p>
      Keep backup copies of important files before testing encryption or
      decryption workflows.
    </p>

    <hr>

    <h2 id="cryptography-notes">Cryptography Notes</h2>

    <p>
      This project is a learning-focused CLI and should be treated as a local
      utility.
    </p>

    <ul>
      <li>
        SHA-256 hashes are one-way values used for hashing and verification.
      </li>
      <li>
        Text encryption uses AES symmetric encryption.
      </li>
      <li>
        File encryption uses AES-based local file encryption.
      </li>
      <li>
        AES is symmetric, so the same secret or derived key material is required
        to decrypt what was encrypted.
      </li>
      <li>
        Local keys, passwords, generated secrets, and sensitive test files should
        be protected and excluded from version control.
      </li>
    </ul>

    <h3>Planned Improvements</h3>

    <ul>
      <li>Cleaner key handling.</li>
      <li>Dedicated test files.</li>
      <li>Clearer file input and output naming.</li>
      <li>Packaged releases through GitHub Releases.</li>
      <li>Expanded Java documentation for future versions.</li>
    </ul>

    <hr>

    <h2 id="project-structure">Suggested Project Structure</h2>

    <pre><code>zencrypt-cli-java/
├── README.md
├── LICENSE
├── .gitignore
└── Zencrypt.java</code></pre>

    <hr>

    <h2 id="building-and-running">Building and Running</h2>

    <p>
      Build the project locally with:
    </p>

    <pre><code>javac Zencrypt.java</code></pre>

    <p>
      Run the compiled class with:
    </p>

    <pre><code>java Zencrypt</code></pre>

    <p>
      If a future version uses Gradle, Maven, or packaged release artifacts, keep
      generated build output separate from the source repository and attach
      distributable files to GitHub Releases.
    </p>

    <hr>

    <h2 id="contributing">Contributing</h2>

    <p align="center">
      <strong>
        Please reach out to verify and validate ideas and contributions before
        continuing any further. Although contributions may be welcome, they should
        stay focused on the Java CLI version of Zencrypt.
      </strong>
    </p>

    <p>
      Recommended workflow:
    </p>

    <ol>
      <li>
        Fork the repository.
      </li>
      <li>
        Create a new branch:
        <pre><code>git checkout -b feature/your-feature-name</code></pre>
      </li>
      <li>
        Make your changes.
      </li>
      <li>
        Confirm that no keys, secrets, generated files, executables, or local test
        files are included.
      </li>
      <li>
        Commit your changes:
        <pre><code>git commit -m "Add your feature"</code></pre>
      </li>
      <li>
        Push to the branch:
        <pre><code>git push origin feature/your-feature-name</code></pre>
      </li>
      <li>
        Open a pull request.
      </li>
    </ol>

    <hr>

    <h1 align="center" id="disclaimer">Disclaimer</h1>

    <p align="center">
      <strong>
        <code>&lt;=&gt; &lt;=&gt; &lt;=&gt; &lt;=&gt; &lt;=&gt; &lt;=&gt; &lt;=&gt;</code>
      </strong>
    </p>

    <p align="center">
      <strong>
        <code>
          This program is provided for educational and demonstration purposes only.
          Use it responsibly and only on files, messages, and systems that you own
          or are authorized to work with.
        </code>
      </strong>
    </p>

    <p align="center">
      <strong>
        <code>
          The project maintainer is not responsible for data loss, misuse, damage,
          or improper use of this software.
        </code>
      </strong>
    </p>

    <p align="center">
      <strong>
        <code>&lt;=&gt; &lt;=&gt; &lt;=&gt; &lt;=&gt; &lt;=&gt; &lt;=&gt; &lt;=&gt;</code>
      </strong>
    </p>

    <hr>

    <h2 id="license">License</h2>

    <p>
      This software is the property of the copyright holder and is protected by
      copyright laws. All rights are reserved by the copyright holder unless explicitly granted in writing.
    </p>

    <p>
      The copyright holder grants no implied or express license for the use,
      copying, modification, distribution, or reproduction of this software, in
      whole or in part, without prior written permission from the copyright holder,
      unless a separate license file states otherwise.
    </p>

    <p>
      Any unauthorized use, copying, modification, distribution, or reproduction of
      this software, in whole or in part, is strictly prohibited and may constitute
      a violation of copyright law.
    </p>

    <p align="center">
      <strong>
        <code>
          By using this software, you acknowledge that you have read and understood
          the terms of this license and agree to comply with all applicable laws.
        </code>
      </strong>
    </p>

    <hr>

    <h2 id="contact">Contact</h2>

    <p>
      For inquiries, suggestions, or project-related questions, contact the project
      maintainer through the Zencrypt Tech organization or open a GitHub issue.
    </p>

    <br>

    <p align="center">
      <strong>Zencrypt Tech</strong>
      <br>
      <em>Keeping It Simple and Secure.</em>
    </p>
  </body>
</html>