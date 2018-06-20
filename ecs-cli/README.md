# Docker ecs-cli image

Build to Docker Image
With https://github.com/aws/amazon-ecs-cli

## Usage

```console
$ docker pull nishigori/awspec

# CMD default is '--version',
$ docker run --rm -it -v ~/.aws:/root/.aws:ro nishigori/ecs-cli
ecs-cli version 1.6.0 (95406b1)

# You can specify args for ecs-cli
$ docker run --rm -it -v ~/.aws:/root/.aws:ro nishigori/ecs-cli --help
NAME:
   ecs-cli - Command line interface for Amazon ECS

USAGE:
   ecs-cli [global options] command [command options] [arguments...]

VERSION:
   1.6.0 (95406b1)

AUTHOR:
   Amazon Web Services

COMMANDS:
     configure  Stores a single cluster configuration.
     up         Creates the ECS cluster (if it does not already exist) and the AWS resources required to set up the cluster.
     down       Deletes the CloudFormation stack that was created by ecs-cli up and the associated resources.
     scale      Modifies the number of container instances in your cluster. This command changes the desired and maximum instance count in the Auto Scaling group created by the ecs-cli up command. You can use this command to scale up (increase the number of instances) or scale down (decrease the number of instances) your cluster.
     ps         Lists all of the running containers in your ECS cluster
     push       Push an image to an Amazon ECR repository.
     pull       Pull an image from an Amazon ECR repository.
     images     List images an Amazon ECR repository.
     license    Prints the LICENSE files for the ECS CLI and its dependencies.
     compose    Executes docker-compose-style commands on an ECS cluster.
     logs       Retrieves container logs from CloudWatch logs. Assumes your Task Definition uses the awslogs driver and has a log stream prefix specified.
     help, h    Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --endpoint value  Use a custom endpoint with the ECS CLI
   --help, -h        show help
   --version, -v     print the version
```

---

## Development

### Requirements

* docker

```
$ docker build -t {APP_NAME} .
```
