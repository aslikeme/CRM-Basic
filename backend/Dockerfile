FROM node:25.6-alpine3.22
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
ENV NODE_ENV=production
RUN addgroup appgroup && adduser -S appuser -G appgroup
USER appuser
EXPOSE 3001
CMD ["node", "server.js"]