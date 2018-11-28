FROM python:2
RUN mkdir /tasks
WORKDIR /tasks

COPY sample-patients-stu3 sample-patients-stu3

RUN cd sample-patients-stu3 && \
    pip install -r requirements.txt && \
    cd bin && \
    python generate.py --write-fhir ../generated --id-prefix smart && \
    cd /tasks && \
    mv sample-patients-stu3/generated patients-stu3 && \
    rm -rf sample-patients-stu3

ENV PATH /tasks:$PATH

COPY load-sample-data-stu3 /tasks/load-sample-data-stu3

CMD ["load-sample-data-stu3"]
