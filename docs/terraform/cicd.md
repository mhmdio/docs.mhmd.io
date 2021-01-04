# Terraform CICD Pipeline

General Workflow for TF CICD.

1. tf env
2. tf init
3. tf fmt
4. tf validate
5. tf lint
6. tf sec / checkov
7. tf plan
8. infracost
9. tf approval
    - Summary

        ```bash
        terraform plan -no-color | grep -E '(^.*[#~+-] .*|^[[:punct:]]|Plan)'
        infracost
        ```

    - chatops = slack/msteams

10. tf apply
11. tf output
12. tf graph
13. chatops = slack/msteams