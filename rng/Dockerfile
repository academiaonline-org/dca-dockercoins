FROM python:3-alpine AS multilayer
RUN pip install Flask
COPY rng.py /

FROM scratch AS prod
COPY --from=multilayer / /

# python rng.py
ENTRYPOINT ["python"]
CMD ["rng.py"]

# optional
EXPOSE 8080
