# Flux Post-processing

## Testing

text jere.

- Post-processing follows the [Swiss Fluxnet Flux Processing Chain](https://www.swissfluxnet.ethz.ch/index.php/data/ecosystem-fluxes/flux-processing-chain/)


## Overview

```{mermaid}
flowchart
L1F[L1 fluxes]
L2QCF[L2 quality flags]
L31F[L3.1 fluxes]
L31Ffiltered[L3.1 fluxes filtered]
L32QCF[L3.2 quality flags]
L33QCF[L3.3 quality flags]
QCF[overall quality flag QCF]
L31FfilteredQCF[L3.1 fluxes filtered with QCF]
L41F[L4.1 gap-filled fluxes]
L42F[L4.2 partitioned fluxes]

L1F --> L2QCF
L2QCF --> L31Ffiltered
L1F --> L31F
L31F --> L31Ffiltered
L31Ffiltered --> L32QCF
L1F --> L33QCF

L2QCF --> QCF
L32QCF --> QCF
L33QCF --> QCF

QCF -- applied to storage-corrected fluxes --> L31FfilteredQCF
L31FfilteredQCF -- gap-filling --> L41F

L41F -- partitioning (NEE) --> L42F

```

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.   

Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.   

Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi.   

Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer