<p align="center">
  <img src="docs/assets/BlobOS_without_border.png" width="128" height="128"/>
</p>
<p align=center>My Operating System</p>

## 💡 About

The point with this project is to learn about operating systems and computers, I don't want to create something huge.

## 🚀 Setup

### 🧾 Dependencies

- [`GCC`](https://gcc.gnu.org/) - C compiler, you'll need it to build the OS.
- [`nasm`](https://nasm.us/) - Assembler, you'll need it to build the OS.
- [`qemu`](https://www.qemu.org/) - Virtualization, for testing the OS without rebooting. _(optional)_

### 🔧 Testing

Option 1: Using `qemu`:

```sh
git clone https://github.com/RedsonBr140/BlobOS.git
cd BlobOS
make
qemu-system-x86_64 -cdrom build/BlobOS.iso -enable-kvm # Runs the project
```

Option 2: Real hardware:

```sh
git clone https://github.com/RedsonBr140/BlobOS.git
cd BlobOS
make
dd if=build/BlobOS.iso of=/dev/yourFlashDrive status=progress
```

> ⚠️ dd is a dangerous command, make sure that you didn't set `of` to any disk with important data, also, it will overwrite anything on the disk, including partitions.
