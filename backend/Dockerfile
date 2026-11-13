FROM node:24-slim
WORKDIR /app
ENV NODE_ENV=production HOST=0.0.0.0
COPY package.json package-lock.json ./
RUN npm ci --omit=dev
COPY dist ./dist
COPY certs ./certs
EXPOSE 3000
CMD ["node", "dist/server.js"]
