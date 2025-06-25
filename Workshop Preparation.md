## 🛠 Workshop Preparation

**Please use macOS or Ubuntu/Linux. Follow the steps below to clone and set up the library:**

---

### 1. Clone the Repository

```bash
git clone git@github.com:coinbase/cb-mpc.git
cd cb-mpc
```

---

### 2. Fetch All Submodules

```bash
git submodule update --init --recursive
```

---

### 3. Enable Git LFS (for accessing PDF documentation)

Install Git Large File Storage (LFS) from [git-lfs.com](https://git-lfs.com/), then run:

```bash
git lfs install
```

---

### 4. Install Required Compilers

* **C++17 Compiler**
  We recommend **Clang v20+**

* **Go Compiler**
  Required to run the demos. Install **Go v1.24**

---

### 5. Install OpenSSL Dependencies

Use the appropriate script based on your OS:

```bash
# For macOS (Intel)
scripts/openssl/build-static-openssl-macos.sh

# For macOS (M1/ARM)
scripts/openssl/build-static-openssl-macos-m1.sh

# For Linux
scripts/openssl/build-static-openssl-linux.sh
```

---

### 6. Build and Test the Library

```bash
make build
make test
sudo make install   # Required for demos to function properly
make demos
```
