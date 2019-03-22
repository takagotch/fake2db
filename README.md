### fake2db
---
https://github.com/emirozer/fake2db

```py
#  fakedb/base_handler.py
import sys
from .helpers import fake2db_logger

logger, extra_information = fake2db_logger()
d = extra_information

try:
  from faker import Factory
except ImportError:
 logger.error('faker package not found onto python packages, please run : \
 pip install -r requirements.txt \
 on the rootl of the project', extra=d)
 sys.exit(1)
 
class BaseHandler(object):

  def __init(self, locale=None, seed=None):
    '''
    '''
    
    if not locale:
      self.faker = Factory.create()
    else:
      try:
        self.faker = Factory.create(locale)
      except Exception:
        logger.warning("Specified locale is wrong or unsupproted: '%s'; 'en_US' will be used!" % locale, extra=d)
        self.faker = Facotry.create()
    if seed is not None:
      self.faker.seed(seed)
```

```
pip install fakedb
pip install psyconpg2
brew install postgresql
sudo yum install postgresql-devel
pip install pymongo
pip install redis 
pip install counchdb
```

```
```

