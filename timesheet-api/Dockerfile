FROM node:20-alpine

# Create app directory
WORKDIR /usr/src/app

# Install dependencies (production only). If you have a package-lock.json use npm ci instead.
COPY package*.json ./
RUN npm install --production --silent

# Copy app sources
COPY . .

# Create a non-root user to run the app
RUN addgroup -S appgroup && adduser -S appuser -G appgroup
USER appuser

# Default port and environment
ENV NODE_ENV=production
ENV PORT=3000

EXPOSE 3000

# Start the server
CMD ["node", "./bin/www"]
