FROM node:lts-alpine
RUN npm install -g pnpm@latest-10
WORKDIR /app/frontend
CMD [ "pnpm", "run", "dev", "--host" ]