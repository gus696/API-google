# API-google
##Documentação 
O código fornecido define uma função search_and_save_info que busca informações sobre um endereço usando a API do Google Maps e salva os detalhes e 
fotos do local em um diretório especificado. A função começa verificando se o diretório de saída existe e, caso contrário, cria-o. Em seguida, 
realiza uma busca pelo endereço fornecido utilizando o método places do cliente googlemaps.

Se a busca não retornar resultados, a função imprime uma mensagem informando que nenhum resultado foi encontrado e retorna. 
Caso contrário, para cada resultado encontrado, a função obtém o place_id e usa-o para buscar detalhes adicionais sobre o local com o método place 
do cliente googlemaps.

Os detalhes do local são então salvos em um arquivo JSON dentro de um subdiretório específico para cada local. Se o local possui fotos, a função itera sobre elas,
construindo a URL para download de cada foto usando o photo_reference e a chave da API. As fotos são baixadas usando a biblioteca requests e salvas no subdiretório 
correspondente. A função imprime mensagens de sucesso ou falha para cada foto baixada.

No início do script, são importadas as bibliotecas necessárias (googlemaps, json, requests, os) e a chave da API do Google Maps é definida. 
O cliente googlemaps é inicializado com essa chave. Por fim, um exemplo de uso da função search_and_save_info é fornecido, buscando informações sobre o endereço 
"vivo Rio de Janeiro" e salvando os resultados no diretório "output".
