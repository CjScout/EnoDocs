# Run a scan
## Instructions
1. Open a terminal![[Pasted image 20240904094649.png]]
2. Nmap commands look like this: ``nmap args XXX.XXX.XXX.XXX/XX``
3. To scan an individual host, use ``XXX.XXX.XXX.XX``
4. To scan a range, use ``XXX.XXX.XXX.XXX/XX`` where ``/XX`` is the relevant subnet mask.
5. Scan outputs will look like this:![[Pasted image 20240904100100.png]]

## Useful arguments

| Argument             | Purpose                                               |
| -------------------- | ----------------------------------------------------- |
| -v or -vv            | Be verbose with logs (or very verbose)                |
| -p * value or range* | Scan a specific port or ports                         |
| -O                   | Attempt host OS detection                             |
| -sV                  | Attempt to determine services available on open ports |
| -sn                  | Skip port scans and just show online hosts            |
