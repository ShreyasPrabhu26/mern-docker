FROM node:20-alpine
RUN addgroup app && adduser -S -G app app
USER app
WORKDIR /app
COPY package*.json ./
USER root
RUN chown -R app:app .
USER app
# install dependencies
RUN npm install
COPY . .
EXPOSE 8000
CMD npm start