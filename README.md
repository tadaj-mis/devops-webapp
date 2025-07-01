services:
  webapi:
    image: sooyaa02/webappandapi:v1.7
    container_name: webapi_container
    restart: always
    # environment:
    #   ConnectionStrings__DefaultConnection: "Host=postgres;Database=mydb;Username=myuser;Password=mypassword"
    #   ASPNETCORE_URLS: "http://+:80" 
    ports:
      - "5239:80"
    networks:
      - mynetwork

networks:
  mynetwork: 
    driver: bridge