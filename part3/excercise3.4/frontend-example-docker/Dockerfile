FROM node:10
WORKDIR /app
COPY . .
EXPOSE 5000
ENV API_URL=http://localhost/api/
RUN npm install && \ 
    apt-get auto-remove && \ 
    rm -rf /var/lib/apt/lists/* && \ 
    useradd -m app && \
    chown -hR app /app
USER app
CMD API_URL=$API_URL npm start
