Add the following to your action:
```
permissions:
      id-token: write   # This is required for requesting the JWT
      contents: read
```

Example usage:
```
- name: AWS Port Forward
        uses: GoodwayGroup/redshift-port-forward-action@main
        with:
          aws-region: REGION
          role-to-assume: IAM_ROLE_TO_ASSUME
          role-session-name: SESSION_NAME
          jumpbox-id: BASTION_HOST_INSTANCE_ID
          redshift-host: YOURHOST.redshift.amazonaws.com
          redshift-port: REDSHIFT_PORT
```
Documentation on oidc via Amazon/Github:

https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services
