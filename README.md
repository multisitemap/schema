# schema.multisitemap.com

+ domain-dns
+ domain-nameserwers
+ ip-server
+ domain-provider.domain-name.nameserwer.server_provider.server_ip


## Manualnie
Mapa może być tworzona odręcznie w celu weryfikacji poprz inframonit.com który używa narzędzia infrash.com do sprawdzenia statusu infrastruktury

## Automatycznie
Mapa może być generowana poprzez skrypty infrash.com
wystarczy podać Endpoint oraz oczekiwane objekty a rezutltaty zostaną wyggenerowane

## Typy kommend infrash

+ compare ( value from in and current infrastructure )
+ load ( from infrastructure )

## Automatyczne generowanie na podstawie pliku CSV

wszystkie dane są dostepne poprzez mikrousluge
lub na serwerze FTP

### IN
dane wejsciowe

```csv
domain,https_status,screenshot_png
example1.com
example2.com
example3.com
```

### STATUS OUT
status wykonyuwania, aktualizowany po kazdej iteracji
```csv
domain,https_status,screenshot_png
example1.com
example2.com
example3.com
```

### DATA OUT
Dane wyjsciowe
```csv
domain,nameservers
example1.com,ns1.com,ns2.com,ns3.com,/home/user/example1.com.png 
example2.com,ns1.com,ns2.com,ns3.com,/home/user/example1.com.png
example3.com,ns1.com,ns2.com,ns3.com,/home/user/example1.com.png
```

Dane wyjsciowe mogą posłużyć do sprawdzenia stanu:

### DATA IN
Dane wejsciowe
```csv
domain,nameservers
example1.com,ns1.com,ns2.com,ns3.com
example2.com,ns1.com,ns2.com,ns3.com
example3.com,ns1.com,ns2.com,ns3.com
```

### DATA OUT
Dane wyjsciowe
```csv
domain,nameservers
example1.com,ns1.com,ns2.com,ns3.com,/home/user/example1.com.png 
example2.com,ns1.com,ns2.com,ns3.com,/home/user/example1.com.png
example3.com,ns1.com,ns2.com,ns3.com,/home/user/example1.com.png
```

## Struktura

multisitemap.com

+ inframonit - monitrowanie infrastruktury za pomocą skryptów i usług SaaS
+ infrash - uruchamianie skryptów

## Examples

### domain-nameserwers

```csv
domain,nameservers
example.com,ns1.com,ns2.com,ns3.com
```
