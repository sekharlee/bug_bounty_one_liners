# subdomains Finder from Rapid dns 

  curl -s "https://rapiddns.io/subdomain/domain.com?full=1#result" | grep "<td>" |grep -v href|grep domain.com|sed 's\<td>\\g'|sed 's\</td>\\g'

# subdomains from securitytrails

curl -s "https://securitytrails.com/list/apex_domain/domain.com" | grep -Po "((http|https):\/\/)?(([\w.-]*)\.([\w]*)\.([A-z]))\w+" | grep ".domain.com" | sort -u
