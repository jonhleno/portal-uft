ARG PLONE_VERSION=6.0.0a6
FROM plone/plone-backend:${PLONE_VERSION}

LABEL maintainer="CDES/STI <desenvolvimento@uft.edu.br>" \
      org.label-schema.name="portal-uft-backend" \
      org.label-schema.description="portal-uft backend image." \
      org.label-schema.vendor="CDES/STI"

# Add local code
COPY . .

# Install local requirements and fix permissions
RUN ./bin/pip install -r requirements.txt \
    && chown -R plone: /app
