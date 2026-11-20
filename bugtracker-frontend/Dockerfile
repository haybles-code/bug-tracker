FROM node:20-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install --legacy-peer-deps \
    && npm install --no-save --legacy-peer-deps @tailwindcss/postcss

COPY . .

# Accept a build argument, needed for deploying on Fly.io
ARG NEXT_PUBLIC_API_URL

RUN echo "test-results.xml" >> .dockerignore

RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]
