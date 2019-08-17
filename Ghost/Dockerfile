FROM ghost:latest

RUN mkdir -p $GHOST_INSTALL/content/adapters/storage/ && \
    npm install ghost-storage-adapter-s3 && \
    cp -r ./node_modules/ghost-storage-adapter-s3 /var/lib/ghost/versions/2.28.0/core/server/adapters/storage/s3

# Define default command
CMD [ "node", "current/index.js" ]
