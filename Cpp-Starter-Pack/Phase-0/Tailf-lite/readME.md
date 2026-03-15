```markdown
# tailf-lite

Tiny utility that follows a growing file and prints appended lines in real time (similar to `tail -f`). Focuses on cross-platform file watching and efficient polling.

Features:
- Follow file growth and print new lines as they are written.
- Optional polling interval and support for file rotation handling.
- Use minimal memory by streaming from file end.

Learning outcomes:
- Learn file seeking (`seek` to file end), robust handling of truncated/rotated logs, and polling vs event-based strategies.
- Practice writing tolerantly for cross-platform differences (Windows vs POSIX file semantics).

Build & run (example):
```sh
g++ -std=c++17 -O2 -o tailf-lite main.cpp
./tailf-lite /var/log/syslog
```

Usage tips:
- Implement rotation detection by monitoring inode/unique file identifiers where available, or fallback to reopen-on-size-decrease logic.
- Provide graceful shutdown handling (Ctrl-C) and optional output timestamps.
```
