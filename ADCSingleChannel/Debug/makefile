################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Drivers/STM32F3xx_HAL_Driver/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
ADCSingleChannel.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
ADCSingleChannel.list \


# All Target
all: ADCSingleChannel.elf secondary-outputs

# Tool invocations
ADCSingleChannel.elf: $(OBJS) $(USER_OBJS) /home/prateek/STM32CubeIDE/workspace_1.0.2/ADCSingleChannel/STM32F303VCTX_FLASH.ld
	arm-none-eabi-gcc -o "ADCSingleChannel.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/home/prateek/STM32CubeIDE/workspace_1.0.2/ADCSingleChannel/STM32F303VCTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="ADCSingleChannel.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

ADCSingleChannel.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "ADCSingleChannel.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
