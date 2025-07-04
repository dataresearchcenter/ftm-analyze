[![ftm-analyze on pypi](https://img.shields.io/pypi/v/ftm-analyze)](https://pypi.org/project/ftm-analyze/)
[![Python test and package](https://github.com/dataresearchcenter/ftm-analyze/actions/workflows/python.yml/badge.svg)](https://github.com/dataresearchcenter/ftm-analyze/actions/workflows/python.yml)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit)](https://github.com/pre-commit/pre-commit)
[![Coverage Status](https://coveralls.io/repos/github/dataresearchcenter/ftm-analyze/badge.svg?branch=main)](https://coveralls.io/github/dataresearchcenter/ftm-analyze?branch=main)
[![AGPLv3+ License](https://img.shields.io/pypi/l/ftm-analyze)](./LICENSE)

# ftm-analyze

Analyze [FollowTheMoney](https://followthemoney.tech) entities. This is part of the ingestion process for [OpenAleph](https://openaleph.org) but can be used standalone or in other applications as well.

`ftm-analyze` outsources the "analyze" pipeline from [ingest-file](https://github.com/openaleph/ingest-file/).

## Features

- Detect language
- Detect country based on location names
- Named Entity Extraction (via [spacy](https://spacy.io/)) and schema prediction
- Convert `Mention` entities into their resolved counterparts if they are known (via [juditha](https://github.com/dataresearchcenter/juditha))
- Extract email, phonenumbers, ibans

## Installation

    pip install ftm-analyze

## Quickstart

    ftm-analyze analyze -i s3://data/entities.ftm.json -o postgresql:///ftm
