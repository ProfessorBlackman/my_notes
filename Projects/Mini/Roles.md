- ADMIN
- BASIC_USER
- PREMIUM_USER
- PERSONA
- SUPER_ADMIN
- SHORT_USER


| ROLE         | PERMISSIONS                                                                                                                                                                        | DESCRIPTION                                                                                                                                                                                                                                         |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ADMIN        | ACCESS_ADMIN, UPGRADE_USER_ACCOUNT, DOWNGRADE_USER_ACCOUNT, ACCESS_USER_ACCOUNT, CRUD_USER                                                                                         | Those with this role are essentially developers working on the platform.                                                                                                                                                                            |
| BASIC_USER   | SHORTEN_URL, MAKE_QR_CODE, BASIC_METRICS,                                                                                                                                          | Can access all features as listed on the pricing page                                                                                                                                                                                               |
| PREMIUM_USER | SHORTEN_URL, MAKE_QR_CODE, FULL_METRICS, <br>CUSTOM_SHORT, CUSTOM_DOMAIN, URL_NOTIFY, CUSTOM_AUTH_PAGE, AUTH_URL, CRUD_PERSONA                                                     | I s a higher end user with access to almost everything on the platform except Admin stuff                                                                                                                                                           |
| PERSONA      | DEFINED BY PREMIUM USER                                                                                                                                                            | This auth entity is meant for granting access to non-registered personnels. So they can perform actions on behalf of the related user. The user will recieve a reccord of their actions on the platform and recieve notifications for major actions |
| SUPER_ADMIN  | ACCESS_ADMIN, REGISTER_ADMIN, UPGRADE_USER_ACCOUNT, DOWNGRADE_USER_ACCOUNT, ACCESS_USER_ACCOUNT, CRUD_USER, <br>CRUD_ADMIN, IMMORTAL, CRUD_SUPER_ADMIN, CRUD_ROLE, CRUD_PERMISSION | This auth entity is the one true admin of this entire platform. He has the ability to control everything and can't be removed by anyone else                                                                                                        |
## NB:
- The role ACCESS_USER_ACCOUNT does not allow it's bearer to enter accounts unauthorized, they will require a permission token or consent from the account owner inorder to access their account.



SENTRY_AUTH_TOKEN=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  
  
REDIS_URI=localhost  
REDIS_PORT=6379  
  
MONGO_URI=localhost  
MONGO_PORT=27017  
MONGO__DB_NAME=mini_base_1  
MONGO_PASS=bdung  
MONGO_USERNAME=mongoadmin  
  
PROMETHEUS_URI=http://localhost:9090  
  
SENTRY_DSN=https://1d566baad63b1f74249d548779623a38@o4506223513239552.ingest.us.sentry.io/4506859455578112  
  
SECRET_KEY=404E635266556A586E3272357538782F413F4428472B4B6250645367566B5970;  
EXPIRATION=86400000;  
REFRESH_EXPIRATION=604800000  
  
DOMAIN=http://localhost:8080  
  
DEBUG=True  
  
ALLOWED_ORIGINS=*  
  
EMAIL_HOST=smtp.gmail.com  
EMAIL_HOST_USER=methuselahnwodobeh@gmail.com  
EMAIL_HOST_PASSWORD=iakwagcpblcikltz  
EMAIL_PORT=587