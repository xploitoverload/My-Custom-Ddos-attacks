# 💣 UDP Flooding Tool — ddos.c
## Developed by [Kalpesh Solanki](https://kalpeshsolanki.me)

# ⚠️ Disclaimer: 
This code performs a UDP flood attack and is intended for educational and ethical testing ONLY.
Unauthorized use against networks is ILLEGAL under most jurisdictions (e.g., Computer Misuse Act, CFAA, etc.).

# 📄 Description
This C program launches a UDP flood attack on a target IP and port for a specified duration using multiple threads. Each thread sends predefined payloads continuously until the time is up.

# 🧠 Features
- UDP socket-based flooding.
- Customizable IP, port, duration, and number of threads.
- Multi-threaded using POSIX pthread.
- Statically linked binary.

# 🔧 Compilation
Use the following `gcc` or `g++` command to compile:
```bash
gcc ddos.c -o fuck -lz -lpthread -static
```
or
```bash
g++ -std=c++14 ddos.cpp -o fuck -pthread
```

- lpthread: Link pthreads for multithreading.
- lz: Links zlib (even if unused, if required by platform).
- static: Produce a statically linked binary (larger but self-contained).

# 🚀 Usage
```bash
./fuck <IP> <PORT> <TIME> <THREADS>
```
## Example
```bash
./fuck 192.168.1.100 80 10 100
```
This will flood 192.168.1.100:80 for 10 seconds using 100 threads.

# 🧵 Threading

Each thread sends all payloads in a loop until the time runs out. Threads are joined after completion to ensure clean exit.

# ⚠️ Legal Warning

- DO NOT use this tool against:
- Servers you do not own
- Networks without permission
- Public IPs

Use this only on authorized test environments (e.g., your own lab setup).

# 📜 Output Example
```text
Flood started on 192.168.1.100:80 for 10 seconds with 100 threads
(XPLOITOVERLOAD)Attack with ID: 139943589336832
...
Attack finished Made By @Kalpesh Solanki
```
# 🧹 Cleanup
No special cleanup required. The socket is closed and memory is freed.

# ✅ License
```text
MIT License

Copyright (c) 2025 KALPESH SOLANKI

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

