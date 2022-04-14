| [![release](https://img.shields.io/github/release/perfsonar/owamp.svg)](https://github.com/perfsonar/owamp/releases) | CentOS        | [![Build Status (CentOS)](https://perfsonar-dev3.grnoc.iu.edu/jenkins/buildStatus/icon?job=owamp-centos)](https://perfsonar-dev3.grnoc.iu.edu/jenkins/view/Debian/job/owamp-centos/) | Debian      | [![Build Status (Debian)](https://perfsonar-dev3.grnoc.iu.edu/jenkins/buildStatus/icon?job=owamp-debian-source)](https://perfsonar-dev3.grnoc.iu.edu/jenkins/view/Debian/job/owamp-debian-source/) |
| -------------|-------------|-------------|-------------|-------------|

# OWAMP

This release is contains implementations of the OWAMP (one-way active measurement protocol) defined by https://tools.ietf.org/html/rfc4656 and the TWAMP (two-way active measurement protocol) defined by https://tools.ietf.org/html/rfc5357

## Code Organization
It is org+anized as follows:

Directory | Description
--- | ---
I2util/ | convienient utility functions... Error reporting, hash funcs...
owamp/ | directory for owamp api - a high level abstraction for speaking the owamp/twamp protocols.
owampd/ | OWAMP and TWAMP server implementations.
owping/ | A command line owamp client (one way ping) and twamp client (two way ping).
powstream/ | A client-daemon for continuous one-way tests. 
conf/ | Example config files. (not installed - EXAMPLES!)
doc/ | html and man page descriptions of owamp and twamp tools.
test/ | unit tests.



git clone --recurse-submodules https://github.com/willendzw/owamp.git



## Q1: ntp_adjtime(&ntp_conf) 获取的NTP配置，

STA_NANO is defined in /usr/include/linux/timex.h

......

#define NTP_API         4       /* NTP API version */

......

#define STA_CLOCKERR    0x1000  /* clock hardware fault (ro) */
#define STA_NANO        0x2000  /* resolution (0 = us, 1 = ns) (ro) */
#define STA_MODE        0x4000  /* mode (0 = PLL, 1 = FLL) (ro) */
#define STA_CLK         0x8000  /* clock source (0 = A, 1 = B) (ro) */



## 01-+2:timex()

  



