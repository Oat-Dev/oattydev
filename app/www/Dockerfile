FROM node:14.18.2-alpine

# ENV NODE_ENV "production"
ENV APP_ENV "production"
ENV NUXT_HOST "0.0.0.0"
ENV TZ "Asia/Bangkok"
ENV PORT=8000

RUN apk --no-cache add curl g++ gcc libgcc libstdc++ linux-headers make pkgconf python3
RUN curl -o- -L https://yarnpkg.com/install.sh | sh

RUN mkdir -p /usr/src/app/www
WORKDIR /usr/src/app/www

COPY package*.json ./
RUN yarn

COPY . .

# RUN yarn --frozen-lockfile --production
# RUN yarn

# RUN yarn build
# RUN npm run build
RUN yarn generate

EXPOSE 8000

CMD yarn start
# CMD npm run start
