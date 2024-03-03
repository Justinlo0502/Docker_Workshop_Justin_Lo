# Front
FROM node:18
COPY ./exercise/frontend /app/
WORKDIR /app
RUN npm install
ENV PORT=3000
CMD [“node”, “index.js”]

# Backend
FROM node:18
COPY backend /app/
WORKDIR /app
RUN npm install
ENV PORT=3000
CMD [“node”, “index.js”]
