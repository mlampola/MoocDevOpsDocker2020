FROM node:10
WORKDIR /app
COPY . .
EXPOSE 8000
ENV FRONT_URL=http://localhost
RUN npm install && \ 
    apt-get auto-remove && \ 
    rm -rf /var/lib/apt/lists/* 
CMD FRONT_URL=$FRONT_URL npm start
