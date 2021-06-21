FROM alpine:3 as base
RUN echo "echo hello world" > greeting.sh
RUN chmod +x greeting.sh

FROM alpine:3.14.0 as final
COPY --from=base greeting.sh /bin/greeting.sh
CMD "/bin/greeting.sh"

FROM final as test
RUN "/bin/greeting.sh"


