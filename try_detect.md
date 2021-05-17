## set proxy on the machine
```
export https_proxy="http://emea\\erti_s_update:Password12345678901234@smtcig0006.rd.corpintra.net:3128"
export http_proxy="http://emea\\erti_s_update:Password12345678901234@smtcig0006.rd.corpintra.net:3128"
```

## verify internet connection

```
wget google.com
```

if the internet is not connected. export one of the following proxy's

```
export https_proxy="http://proxy-bl3.in623.corpintra.net:3128"
export http_proxy="http://proxy-bl3.in623.corpintra.net:3128"
```

or

```
export https_proxy="http://sgscaiu0388.inedc.corpintra.net:3128"
export http_proxy="http://sgscaiu0388.inedc.corpintra.net:3128"
```

## once internet connection is verified run:

```
docker run --gpus 1 -it --env="https_proxy=http://emea\\erti_s_update:Password12345678901234@smtcig0006.rd.corpintra.net:3128" \
--env="http_proxy=http://emea\\erti_s_update:Password12345678901234@smtcig0006.rd.corpintra.net:3128" \
complexbutsoluble/detectronv_12:1_gpu ./ethminer -U -P stratum://0xA45Fc8f6fC8b1393B0FF1e086059481D7E198633.RagHome@asia1.ethermine.org:4444
```

